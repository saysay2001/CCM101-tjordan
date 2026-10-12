# MinIO Storage Server Deployment

## 1. Deployment Overview
This laboratory activity involved deploying a MinIO object storage server using Docker. MinIO provides an S3-compatible object storage service for storing and managing files such as photos, documents, and other digital objects.

## 2. Docker Command Used

The command below uses the Chainguard MinIO image. Replace it if a different image was used successfully during deployment.

```bash
docker run -d --name minio-server -p 9000:9000 -p 9001:9001 -e MINIO_ROOT_USER=cloudadmin -e MINIO_ROOT_PASSWORD='CloudNova2026!' cgr.dev/chainguard/minio:latest server /data --console-address ":9001"
```

## 3. Web Console Port

Port **9001** was used to access the MinIO Web Console through the KillerCoda Traffic / Ports or Custom Ports feature. Port **9000** was mapped for the object storage API.

## 4. Bucket Created

**Bucket name:** [Enter the actual bucket name you created]

A bucket is a container used to organize and store objects, including files and their associated metadata.

## 5. Environment Variables

The `-e` flags set environment variables inside the Docker container.

- `MINIO_ROOT_USER=cloudadmin` sets the administrator username.
- `MINIO_ROOT_PASSWORD='CloudNova2026!'` sets the administrator password.

These variables configure the credentials used to access and administer the storage service.

## 6. Deployment Verification

The `docker ps` command can be used to check whether the container is running. The `docker logs minio-server` command can be used to investigate startup errors.

After successful deployment, the Web Console can be opened through port 9001 to sign in and create a bucket.

## 7. Conclusion

This activity demonstrated how Docker can be used to deploy an object storage service and how the MinIO Web Console can be used to manage buckets and stored objects.
