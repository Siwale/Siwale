# Designing for Solar-Powered Infrastructure  

## Key Constraints in Zambia  
- **Voltage Fluctuations**: 160V-260V swings damage servers.  
- **Battery Life**: Avg. 4h backup on cloudy days.  

## My Software Adaptations  
1. **Graceful Degradation**:  
   ```javascript
   // Check solar battery levels via GPIO
   setInterval(async () => {
     if (await getBatteryLevel() < 15%) {
       await enterLowPowerMode(); // Close non-critical DB connections
     }
   }, 30000);