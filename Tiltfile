def create_namespace(name):
    k8s_yaml(blob("""apiVersion: v1
kind: Namespace
metadata:
  name: %s
""" % name))

name = "prometheus-test"

create_namespace(name)

k8s_yaml(helm("charts/kube-prometheus-stack", name, namespace = name))
