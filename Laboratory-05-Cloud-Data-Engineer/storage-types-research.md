# Checkpoint 2: Research on Types of Cloud Storage

## Introduction

Cloud storage allows organizations to store and access data using cloud-based infrastructure. The three primary types are block storage, file storage, and object storage. Each has different characteristics and is designed for specific storage requirements.

## Comparison of Cloud Storage Types

| Storage Type | Description (How It Stores Data) | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| **Block Storage** | Divides data into fixed-sized blocks, with each block managed and addressed separately. | Virtual machine disks, operating systems, and databases that require low-latency access. | Amazon Elastic Block Store (Amazon EBS) |
| **File Storage** | Organizes data into files and directories using a hierarchical folder structure. | Shared folders, document management, and applications that need shared file access. | Amazon Elastic File System (Amazon EFS) |
| **Object Storage** | Stores data as objects containing the data itself, metadata, and a unique identifier inside a bucket. | Images, videos, backups, documents, and other large collections of unstructured data. | Amazon Simple Storage Service (Amazon S3) |

## Recommendation to the Client

Object Storage is the best choice for the client's photo-sharing application because it is designed to store large amounts of unstructured data, including millions of user-uploaded images. It allows images to be organized into buckets and accessed through APIs, making it suitable for integration with web applications. It can also scale as the collection of photos grows without requiring the images to be stored inside temporary web server containers.

## Conclusion

Block storage is suitable for disks and databases, file storage is useful for shared files and folders, and object storage is ideal for large collections of unstructured data. For this project, object storage provides the most appropriate foundation for storing user-uploaded photos.

## References

- Amazon Web Services. (n.d.). *What is cloud storage?* https://aws.amazon.com/what-is-cloud-storage/
- Amazon Web Services. (n.d.). *What is Amazon S3?* https://aws.amazon.com/s3/
- Amazon Web Services. (n.d.). *What is Amazon EBS?* https://aws.amazon.com/ebs/
- Amazon Web Services. (n.d.). *What is Amazon EFS?* https://aws.amazon.com/efs/
