# Build Docker image
docker_build('izanami',
             context='.',
             dockerfile='./Dockerfile',
)

# Config
KUBERNETS_DIR="./resources"
manifests = listdir(KUBERNETES_DIR)

# Apply Kubernetes manifests
# Allow duplcates is marked true for when you import multiple go-micro Tiltfiles
#  into a single Tiltfile it will mark the clusterrole as duplicate.
k8s_yaml(manifests, allow_duplicates=True)
