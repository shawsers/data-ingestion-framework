FROM quay.io/operator-framework/helm-operator:v0.19.2
MAINTAINER Meng Ding <meng.ding@turbonomic.com>

# Required OpenShift Labels
LABEL name="Turbodif Operator" \
      vendor="Turbonomic" \
      version="v7.22.0" \
      release="1" \
      summary="This is the turbodif operator." \
      description="This operator will deploy an instance of turbodif." \
### Required labels above - recommended below
      url="https://www.turbonomic.com" \
      run='docker run -tdi --name ${NAME} turbonomic/turbodif-operator:7.22' \
      io.k8s.description="Turbonomic Workload Automation Platform simultaneously optimizes performance, compliance, and cost in real-time. Workloads are precisely resourced, automatically, to perform while satisfying business constraints.  " \
      io.k8s.display-name="Turbodif Operator" \
      io.openshift.expose-services="" \
      io.openshift.tags="turbonomic, Multicloud Container"

# Required Licenses
COPY licenses /licenses

COPY watches.yaml ${HOME}/watches.yaml
COPY helm-charts/ ${HOME}/helm-charts/
