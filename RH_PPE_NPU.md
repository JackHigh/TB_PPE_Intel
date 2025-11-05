



Model Conversion Error

sudo dnf install git-lfs
  git lfs pull

  cd models/
  yolo export model=model.pt format=openvino


podman Error
 podman network create shared

  podman run -d --replace --privileged     --name ppe-detector     -p 5000:5000     --device /dev/dri:/dev/dri     --group-add keep-groups     --device /dev/video0:/dev/video0     -v "$(pwd)/models":/app/models     -e CAM_INDEX="/dev/video0"     -e MQTT_BROKER="<BROKER_IP>"     -e MODEL_PATH="/app/models/model_openvino_model"     --network shared     localhost/ppe-detector

Flux Error
mkdir -p FUXA/fuxa_appdata FUXA/fuxa_db FUXA/fuxa_logs FUXA/fuxa_images