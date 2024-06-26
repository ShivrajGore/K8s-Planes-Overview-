
![image](https://github.com/ShivrajGore/K8s-Planes-Overview-/assets/20918004/69b2f643-cabd-418e-a14a-34db9e8242e3)

**K8s -**
**Component in worker node:** (_Data plane_- Responsible for running your application)

**1. Kubelet:** is responsible for starting, stopping, and managing containers on a node. It interacts with the container runtime (such as Docker, containerd, or CRI-O) to create, delete, and monitor containers. Overall, kubelet plays a critical role in ensuring the proper functioning and health of containers within a Kubernetes cluster.
   
**2. Kubeproxy:**
Load Balancing: When a service has multiple pods backing it, kube-proxy performs load balancing to distribute incoming requests evenly among those pods. This helps in optimizing resource utilization and ensures high availability and scalability of the application.Overall, kube-proxy plays a crucial role in providing networking capabilities to Kubernetes applications, enabling seamless communication and load balancing across containers and services within the cluster.

**3. Container runtime:** In Kubernetes (K8s), a container runtime is the software responsible for running containers. Kubernetes is designed to be container-runtime agnostic, meaning it can work with different container runtimes. The most common container runtimes used with Kubernetes are Docker, containerd, and CRI-O.

--------------------------------------------------------------------------------------------------------------

**Component in Master node:** (_Control plane_- Controlling all the actions)
In Kubernetes (K8s), the control plane is responsible for managing the cluster and orchestrating containerized applications.

**1. API Server:** The API server acts as the front end for the Kubernetes control plane. It exposes the Kubernetes API, which users, administrators, and other parts of the system interact with to manage the cluster. The API server validates and processes API requests, stores the cluster state in etcd, and enforces authentication and authorization policies.

**2.Scheduler:** The scheduler is responsible for placing newly created pods onto nodes in the cluster.The scheduler ensures that pods are distributed across the cluster in a balanced and efficient manner.

**3. Controller Manager:** The controller manager is a collection of controllers that regulate the state of the cluster and perform cluster-wide functions.These controllers continuously monitor the cluster state through the API server and take corrective actions to maintain the desired state.

**4. etcd:** etcd is a distributed key-value store used as the cluster's primary data store. It stores the persistent cluster state, including configuration data, secrets, and metadata about pods, services, nodes, and more. The control plane components read from and write to etcd to maintain a consistent and up-to-date view of the cluster.

**5. Cloud Controller Manager (Optional):** The Cloud Controller Manager is an optional component responsible for interacting with the underlying cloud provider's APIs to manage resources such as load balancers, volumes, and instances. 
