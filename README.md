# Requirements
- Python
  - Scipy
  - Pandas
  - Numpy
  - Matplotlib
- Rust
- Rerun.io

# Usage
1. Get multiple laptops to use as clients. Mark a grid and place the laptops in arbitrary positions within that grid.
2. Run the **voice_direction_finder** project using *cargo run* modifying the TCP address to that of the server.
3. Now run the python server in the *Python_server* repo from any computer by using *python3 dataCollector.py*.
4. Place a sound source in a known position and do this multiple times for multiple data points.
5. Run *python3 optimzer.py* in the **Python server** repo.
6. This gives sensor{n}.csv file for all n sensors.
7. For the $i^{th}$ sensor, place the sensor{i}.csv file into the **voice_direction_finder** repo by renaming the file to *params.csv*.
8. Now provided that the sensor positions are static, we can run either the Kalman Filter by running the **VoiceLocalizerEKF** repo or use centroid polygon mehtod by running **rust_server** repo.
9. Now a sound source with sufficiently high bandwidth within the grid can be localized.
