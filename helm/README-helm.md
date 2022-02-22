# umbrella-ci-cd helm


This helm project is to show how you may use umbrella charts to manage your companies cicd processes for several products in a general solution. The objective is to standardize the cicd process to get economies of scale within the organisation.

The scope of the porject includes:
-helm charts

#Tips
- update helm charts recursively
find ./helm -name Chart.yaml -print | sed s/Chart.yaml//g | awk -F"/" '{print NF $0}' | sort -nr | sed 's/^.//' | xargs -n1 helm dep build

- develop your computed values tree for your umbrella templates
helm install test ./helm --dry-run --debug



