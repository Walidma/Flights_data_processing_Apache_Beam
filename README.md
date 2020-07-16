# Flights_data_processing_Apache_Beam


Manage config configurations :  
export PROJECT_ID=$(gcloud info --format='value(config.project)')  
export BUCKET=${PROJECT_ID}  
  
Run on dataflow :  
mvn compile exec:java  -Dexec.mainClass=com.google.cloud.training.flights.CreateTrainingDataset -Dexec.args="--project=$PROJECT_ID --bucket=$BUCKET --fullDataset=true --maxNumWorkers=4 --autoscalingAlgorithm=THROUGHPUT_BASED"
