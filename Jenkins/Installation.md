## Jenkins Installation Steps

1. **Update package list**
   ```bash
   sudo apt update
   ```

2. **Install OpenJDK 17**
   ```bash
   sudo apt install openjdk-17-jdk
   ```

3. **Verify Java installation**
   ```bash
   java --version
   ```

4. **Add Jenkins repository key**
   ```bash
   curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo tee \
     /usr/share/keyrings/jenkins-keyring.asc > /dev/null
   ```

5. **Add Jenkins repository**
   ```bash
   echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
     https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
     /etc/apt/sources.list.d/jenkins.list > /dev/null
   ```

6. **Update package list again**
   ```bash
   sudo apt update
   ```

7. **Install Jenkins**
   ```bash
   sudo apt install jenkins
   ```

8. **Enable Jenkins service**
   ```bash
   sudo systemctl enable jenkins
   ```

9. **Start Jenkins service**
   ```bash
   sudo systemctl start jenkins
   ```

10. **Access Jenkins**
    - Open your browser and go to: [http://localhost:8080/](http://localhost:8080/)

11. **Get the initial admin password**
    ```bash
    sudo cat /var/lib/jenkins/secrets/initialAdminPassword
    ```