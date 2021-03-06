Scale an opsworks layer with ruby aws-sdk

I use this to work around the opsworks scaling limitations. I trigger this script with sensu remedations.

Command line example

```
scaleOpsworksLayer.rb -s opsviz -r us-east-1 -l ElasticSearch -i 2 -m 5 -t m3.medium -z subnet-aaaaaa,subnet-bbbbbb,subnet-cccccc
```

Parameters

```
-s --stackname:         your stack name
-r --region:            the region your stack is running in
-l --layername:         the name of the layer you want to scale
-i --instancecount:     scale by this number of instances
-m --maxinstancecount:  do not scale over this maximum number of instances in a layer
-t --instancetype:      the aws instance type
-z --subnetids SUBNETIDS  and array of subnet ids. instances will be spun up in the subnet with the least amount of instances
```

Optional Parameters (if not specified will be using your IAM instance profile)

```
-x --accesskey AWS_ACCESSKEY
-y --secretkey AWS_SECRETKEY

```
