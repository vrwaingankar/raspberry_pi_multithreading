# raspberry_pi_multithreading
by using a dedicated thread (separate from the main thread) to read frames from our camera sensor, we can dramatically increase the FPS processing rate of our pipeline. This speedup is obtained by  
(1) reducing I/O latency and  
(2) ensuring the main thread is never blocked, allowing us to grab the most recent frame read by the camera at any moment in time.  
Using this multi-threaded approach, our video processing pipeline is never blocked, thus allowing us to increase the overall FPS processing rate of the pipeline. 
