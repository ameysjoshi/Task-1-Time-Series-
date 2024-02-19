# Task-1-Time-Series-
The task is to write an algorithm that reads the data sequentially (one by one) according to  timestamp and clusters the data coming from different sensors (use sensor_id) and saves the  fused data to a new CSV file where each entry should have f_timestamp, f_id, cluster_data,  f_u_id.

I have used DBSCAN algorithm for the task. Numpy and Pandas libraries are used for data handling and manipulation. 
The data from the test_Data_1 CSV file is loaded and sorted by timestamp_id to ensure sequential handling. The necessary parameters for DBSCAN algorithm are defined and clustering is performed.

The code tries to determine the unique_id for each cluster. If the clustered items have the same unique_id then that id is assigned as unique_id to that cluster. If the clustered items have different unique_id then -1 is assigned as unique_id to that cluster. This means we don't have further information about the similarity of the objects clustered together. A random f_id is also assigned to each cluster. 
The clustering results are stored into a new data frame and an output CSV file is created. 
