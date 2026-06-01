# no2-o3-calibration

- rooftop analysis from Amy, make sure that the values aren't too crazy? This might be the hardest part of this process

- reach out to quantAQ to get update calibrations for MJF
- reach out to paul to grab NO2 data from november and december onwards at MJF
- Split reference data from AS and ND separately, filter out values based on Paul's recommendations (might have to be manual), ignore negative values (can code this)
- Get QuantAQ NO2 data from three sensors for AS and four sensors for ND (ALL IN HOURLY FORMAT)
- Check for flatline values in the quantNO2 data (should be good as long as the calibration is updated). Filter if present (will be a little weird on hourly format but will work)
- Filter out low RSD times and identify them in a CSV
- Ensure that the NO2 values from Paul are in the right UTC time format
- Isolate NO2 values from Paul's data based on times from the QAQ output
- Now reference data has been isolated in an hourly format. Download raw beacon data in hourly format
- Set up training-testing CSV for the process
- Start with calibrating the EP site, and check performance. Try doing MLR and XGBoost
- Calibration scheme should work fine because the data is so normally distributed, at least at MJF. Once it's determined that the calibration works well then we move on to the other sites, using the same model. Ensure that all the data is downloaded properly for calibrating
