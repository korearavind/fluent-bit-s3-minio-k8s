# fluent-bit_s3_minio_on_k8s
This document helps you deploy the fluent-bit image in k8s for the minIO

        bucket bucket_details 
        endpoint URL
        total_file_size 5M
        store_dir /buffer/dir/path/
        s3_key_format /to/the/path/file_%Y%M%D.log
        static_file_path true

a. Add the Minio bucket details in - **bucket bucket_details** .

b. Add the endpoint of the minio bucket - ****endpoint URL****.

c. Add the path of the bucket, the location where you want to save the files in - **s3_key_format /to/the/path/file_%Y%M%D.log**.

Add the environmental variables 

    - name: AWS_ACCESS_KEY_ID
      value: " AWS_ACCESS_KEY_ID_value " #add the access key details of MINIO
    - name: AWS_SECRET_ACCESS_KEY
      value: " AWS_SECRET_ACCESS_KEY_value"  #add the secret key details of MINIO
