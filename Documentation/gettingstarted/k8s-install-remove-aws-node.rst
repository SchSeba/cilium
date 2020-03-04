Cilium will manage ENIs instead of VPC CNI, so it the ``aws-node`` DaemonSet
has to be delete to prevent conflict behaviour.

.. note::

   Once ``aws-node`` DaemonSet is deleted, EKS will not try to restore it.

.. code:: bash

   kubectl -n kube-system delete daemonset aws-node
