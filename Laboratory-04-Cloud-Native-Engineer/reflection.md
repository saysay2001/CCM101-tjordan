# Reflection

This laboratory helped me understand why containerization is becoming an important part of modern software development and IT operations. One of the biggest differences I noticed between Docker containers and Virtual Machines is the boot and setup process. A Virtual Machine needs to start a complete operating system, which requires more time and system resources. In contrast, a Docker container uses the host operating system's kernel and can start within seconds. With Docker, I was able to pull the Nginx image and deploy a working web server using only a few commands.

Port mapping such as `-p 8080:80` is necessary because the Nginx web server is running inside the container on port 80, while I access the service through port 8080 on the host. The mapping connects the host's port 8080 to the container's port 80, allowing an HTTP request such as `curl http://localhost:8080` to reach the Nginx server.

I also learned that using `docker rm` removes the container itself. Any data stored only inside the container's writable layer is removed when the container is deleted. This shows why persistent application data should be stored using appropriate Docker volumes or external storage when the data needs to survive the container lifecycle.

Containerization can also improve collaboration between developers and IT operations teams. Developers can package an application together with its dependencies, while operations teams can deploy the same containerized application consistently across environments. This supports DevOps practices by reducing environment-related problems and making deployment, testing, and scaling more efficient.

My GitHub portfolio is also evolving from simply containing individual projects into a record of my technical learning and practical experience. By documenting laboratories, commands, screenshots, and reflections, I can demonstrate not only the applications I have created but also my ability to work with modern technologies such as Docker and cloud-native tools. This makes my portfolio more organized and useful for showing my growth as an IT student.

