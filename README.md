## Kubeadm Cluster Setup Scripts

Here is the supporting documentation and video demo.

1. [Documentation - Kubeadm Cluster Setup Guide](https://devopscube.com/setup-kubernetes-cluster-kubeadm/)
2. [Kubeadm workflow explanation and demo video](https://youtu.be/xX52dc3u2HU)

The common.sh script should be run on master and any worker node that will be added.
to join a workker node to control plane run the following command on control plane server to generate a command with token that we will be used while joining:
```bash
kubeadm token create --print-join-command
```
After running that you will get a result like that:
```bash
sudo kubeadm join 10.128.0.37:6443 --token j4eice.33vgvgyf5cxw4u8i --discovery-token-ca-cert-hash sha256:37f94469b58bcc8f26a4aa44441fb17196a585b37288f85e22475b00c36f1c61
```
That command you will execute it inside each worker node server to join it the control plane running.

## For Kubernetes Certification Aspirants

If you are preparing for CKA, CKAD, CKS, or KCNA exam, **save 20%** today using code **DCUBE20** at https://kube.promo/devops. It is a limited-time offer. Or Check out [Linux Foundation coupon](https://scriptcrunch.com/linux-foundation-coupon/) page for the latest voucher codes.


