# Get Started with Dataplex: Challenge Lab || [ARC117](https://www.cloudskillsboost.google/focuses/62710?parent=catalog) ||

# # Like, comment, share & Don't forget to subscribe [Qwiklab_Explorers_ts](https://youtube.com/@titashshil?si=RgamNu1dc9jVIbJN) 👍😄🤝

### Run the following Commands in CloudShell

```
export LOCATION=
```
```
export ID=$DEVSHELL_PROJECT_ID

gcloud services enable datacatalog.googleapis.com
gcloud services enable dataplex.googleapis.com

gcloud dataplex lakes create customer-engagements \
   --location=$LOCATION \
   --display-name="Customer Engagements"

gcloud dataplex zones create raw-event-data \
    --location=$LOCATION \
    --lake=customer-engagements \
    --display-name="Raw Event Data" \
    --type=RAW \
    --resource-location-type=SINGLE_REGION \
    --discovery-enabled

gsutil mb -p $ID -c REGIONAL -l $LOCATION gs://$ID

gcloud dataplex assets create raw-event-files \
--location=$LOCATION \
--lake=customer-engagements \
--zone=raw-event-data \
--display-name="Raw Event Files" \
--resource-type=STORAGE_BUCKET \
--resource-name=projects/my-project/buckets/${ID}
```

### Task 3. Create and apply a tag template to a zone

- Go to Templates from [here](https://console.cloud.google.com/dataplex/templates/create)

-  follow next steps carefully from video!

### Congratulations 🎉 for completing the Lab !

##### *You Have Successfully Demonstrated Your Skills And Determination.*

#### *Well done!*

#### Don't Forget to Join the [Telegram Channel](https://t.me/quickgcplab) & [Discussion group](https://t.me/quickgcplabchats)

# [QUICK GCP LAB](https://www.youtube.com/@quickgcplab)
