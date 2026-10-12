# Laboratory 5: The Cloud Data Engineer

## Mission Brief

This laboratory activity focuses on deploying an S3-compatible object storage service using MinIO and Docker.

The scenario involves a client developing a photo-sharing application that needs reliable storage for millions of uploaded images. The objective is to demonstrate how object storage can keep uploaded files separate from temporary web server containers, making storage easier to manage and scale.

## Mission Overview

The mission is to explore cloud storage technologies and deploy a MinIO object storage server in a Linux environment using Docker. Through this activity, the learner will investigate different storage types, configure the storage service, access its management console, and create a bucket for storing client photos.

The activity also emphasizes troubleshooting, technical documentation, data reliability, and the importance of protecting credentials when working with cloud infrastructure.

## Objectives

- Differentiate block, file, and object storage.
- Deploy MinIO using Docker.
- Access the MinIO management console.
- Create a bucket named `client-photos`.
- Upload and verify a test file.
- Understand Docker port mapping and environment variables.
- Document the implementation with screenshots and Markdown.
- Identify basic security practices for managing cloud storage.

## Laboratory Checkpoints

- **Checkpoint 1:** Expand Your Cloud Portfolio
- **Checkpoint 2:** Research Storage Types
- **Checkpoint 3:** Deploy MinIO
- **Checkpoint 4:** Create the Bucket and Upload a File
- **Checkpoint 5:** Document Results and Reflection

## Tools and Technologies

- **KillerCoda** — provides the cloud-based Linux terminal environment.
- **Docker** — runs the MinIO storage service inside a container.
- **MinIO** — provides S3-compatible object storage and a management console.
- **GitHub** — stores and manages the laboratory documentation and project files.
- **Markdown** — formats the README, deployment documentation, and reflection.
- **Web Browser** — accesses the MinIO management console.

## Skills Learned

- Executing Docker commands in a Linux terminal.
- Deploying and managing containerized applications.
- Configuring environment variables and port mappings.
- Troubleshooting Docker image pull and container startup errors.
- Understanding the differences between block, file, and object storage.
- Creating buckets and managing stored objects.
- Verifying uploaded files through a storage management interface.
- Documenting technical procedures and laboratory results using Markdown.
- Applying basic security practices when handling credentials.
- Understanding the importance of redundancy, backups, and disaster recovery in cloud storage.

## Evidence

Screenshots documenting each applicable checkpoint will be stored in the `screenshots/` folder.

The evidence may include:

- Docker deployment command and successful container status.
- MinIO Web Console login and dashboard.
- The created `client-photos` bucket.
- The uploaded test file and its successful verification.
- Relevant terminal commands and outputs.

## Laboratory Deliverables

The laboratory folder should contain the following files and resources:

- `README.md` — mission overview, objectives, tools, skills learned, and evidence.
- `minio-deployment.md` — technical deployment steps, exact Docker command, console port, bucket name, and environment variable explanations.
- `reflection.md` — a 250–350-word reflection answering the required questions about object storage, Docker, buckets, data protection, and Linux command-line confidence.
- `screenshots/` — screenshots demonstrating the completed checkpoints.

## Security Note

Credentials, passwords, and secret keys must not be included in public repository files or screenshots. Use placeholders in documentation whenever necessary, and avoid committing real credentials to GitHub.

## Expected Laboratory Output

Upon successful completion, the laboratory should demonstrate a running MinIO storage server, access to the management console, a bucket named `client-photos`, and a verified uploaded test file.

The documentation and screenshots should provide evidence of the implementation and explain the concepts and skills learned throughout the activity.

## Conclusion

This laboratory introduces practical cloud data engineering concepts through the deployment of MinIO using Docker. It demonstrates how object storage can organize and manage large collections of files while highlighting the importance of reliable deployment procedures, data protection, troubleshooting, and clear technical documentation.
