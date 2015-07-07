Scale an opsworks layer with ruby aws-sdk


Command line example

```
scaleOpsworksLayer.rb -s opsviz -r us-east-1 -l ElasticSearch -i 2 -m 5 -t m3.medium
```

Parameters

```
-s --stackname STACKNAME
-r --region REGION
-l --layername LAYERNAME
-i --instancecount INSTANCECOUNT
-m --maxinstancecount MAXINSTANCECOUNT
-t --instancetype INSTANCETYPE
```