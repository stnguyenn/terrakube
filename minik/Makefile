
MK=minikube
KC=kubectl
TF=terraform
TP=miniplan
CL=curl

default:
	@echo 👋 terra-minik

cluster:
	@$(MK) delete
	@$(MK) start

init:
	@$(TF) init

plan:
	@$(TF) plan -out $(TP)

apply: init plan
	@$(TF) apply $(TP)

get_nginx:
	@$(KC) get all -n nginx

mini_svc_nginx:
	@$(MK) service -n nginx nginx 

curl_nginx:
	@$(CL) `$(minikube ip)`:$(XP)

