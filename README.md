gcloud init

gcloud auth login

gcloud auth list



gcloud config set account 'ACCOUNT'

gcloud projects list


gcloud config set project 'ID-PROJECT'

gcloud billing accounts list


gcloud config get-value project


gcloud billing budgets create \
--billing-account='BILLING-ACOUNT' \
--display-name="Budget Cloud-1" \
--budget-amount=263EUR \
--filter-projects=projects/cloud-1 \
--threshold-rule=percent=0.1 \
--threshold-rule=percent=0.3 \
--threshold-rule=percent=0.5 \
--threshold-rule=percent=0.9

gcloud billing budgets list --billing-account='BILLING-ACCOUNT'


gcloud billing budgets delete 'NAME-BUDGET' --billing-account='BILLING-ACCOUNT'

gcloud compute addresses create cloud-1-ip --region=europe-west9

gcloud compute addresses describe cloud-1-ip --region=europe-west9 --format="get(address)"

gcloud compute instances create cloud-1-instance --address='IP' --tags="cloud-1-web" --image=debian-13-trixie-v20260714 --image-project=debian-cloud --zone=europe-west9-b --machine-type=e2-medium

gcloud compute firewall-rules create allow-http-https-ssh --target-tags=cloud-1-web --action=allow --rules=tcp:80,tcp:443,tcp:22


gcloud compute ssh --project='ID-PROJECT' --zone=europe-west9-b 'INSTANCE'


ansible-galaxy collection install -r ansible/requirements.yml

ansible-playbook ansible/site.yml
