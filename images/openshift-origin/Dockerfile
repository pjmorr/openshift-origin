FROM openshift/origin:v1.5.1

RUN \
  curl -L https://github.com/cloudnautique/giddyup/releases/download/v0.14.0/giddyup -o /usr/bin/giddyup && \
  chmod +x /usr/bin/giddyup && \
  yum install -y jq unzip python-pip && \
  pip install PyYAML

WORKDIR /etc/origin
ADD run.sh configure.py examples_v1.5.tgz kubeconfig users.htpasswd /
ENTRYPOINT ["/run.sh"]
