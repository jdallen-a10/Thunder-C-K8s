# Thunder-C-K8s
Example Kubernetes manifest files to start up A10 Thunder Container v5.2.0

A couple of notes:
1.  In the `annotations:` section, there are three Prometheus lines that allow Prometheus to collect metrics from Thunder Container once it starts up.
2.  Thunder Container needs to be a "priviliaged" container in order to run and act as a CNF.
3.  There is a `startupProbe:` section that will let Kubernetes know when Thunder Container is ready to start processing network traffic.
4.  There are two additional networks defined in the `annotations:` section.  This allows for processing of network traffic as a normal ADC would, with an inbound traffic interface, and an outbound traffic interface. This manifest file also assumes an MGMT interface using the default Kubernetwork network.


