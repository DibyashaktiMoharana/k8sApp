# Node.js Kubernetes Deployment

## Steps to Deploy

1. **Build Docker Image:**
   ```sh
   docker build -t your-dockerhub-username/node-app .
   ```

2. **Push to Docker Hub:**
   ```sh
   docker push your-dockerhub-username/node-app
   ```

3. **Deploy to Kubernetes:**
   ```sh
   kubectl apply -f deployment.yaml
   kubectl apply -f service.yaml
   kubectl apply -f hpa.yaml
   kubectl apply -f configmap.yaml
   kubectl apply -f secret.yaml
   kubectl apply -f persistent-volume.yaml
   kubectl apply -f persistent-volume-claim.yaml
   ```

4. **Verify Deployment:**
   ```sh
   kubectl get pods
   kubectl get services
   ```

5. **Test Application:**
   ```sh
   curl http://<EXTERNAL-IP>:<PORT>
   ```

   [Download Deployment Files](https://drive.google.com/file/d/1W_b4yx5bMJKRLg8Ywpv7s4yNFD__Gf7B/view?usp=sharing)