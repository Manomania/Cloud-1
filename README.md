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


