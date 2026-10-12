# Mission Reflection: Cloud Data Engineering

This laboratory activity helped me understand how object storage works and how Docker can make cloud storage deployment easier. It also improved my confidence in using the Linux command line.

Object storage is better suited for storing millions of photos because it organizes files as individual objects with unique identifiers and metadata. Unlike traditional block storage, which manages data in fixed-sized blocks, object storage is designed to handle large amounts of unstructured data. It also makes it easier to organize, retrieve, and scale storage as the number of photos increases. This makes object storage useful for social media platforms, businesses, and websites that manage many images.

Using Docker made deploying the MinIO storage server easier because it allowed me to run the application inside a container without manually installing and configuring every component. With a single Docker command, I could specify the image, map the ports, and configure the administrator credentials. Although I encountered an image pull error, troubleshooting the problem helped me understand that the correct image source is important when deploying a container.

In cloud storage, a bucket is a container used to organize objects such as photos, documents, and videos. It provides a structured way to manage stored files and their associated information.

Large enterprise companies protect their object storage data through redundancy, replication, backups, and disaster recovery plans. They may store copies of their data across different servers or geographic locations. Therefore, if one physical server crashes, another copy may still be available. Monitoring systems and regular recovery testing also help ensure data availability and reliability.

Lastly, this activity gradually increased my confidence in navigating the Linux command line. At first, executing Docker commands and understanding error messages felt challenging. However, by examining the errors and trying alternative solutions, I learned the importance of patience, accuracy, and troubleshooting. I realized that learning cloud data engineering involves more than memorizing commands; it also requires understanding what each command does and how to solve problems independently. I look forward to applying these skills in future cloud computing and system administration activities.
