## TODO

https://github.com/AfterShip/spot-cluster/issues/1

## What it does by spot-cluster?

Auto manage AWS spot instance cluster by evenly distributed to zones and types.


![image](https://cloud.githubusercontent.com/assets/1013507/10987920/ac4471e2-8472-11e5-8c4f-b3328398ed86.png)


## AWS IAM

#### Role
```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "Stmt1435887829000",
            "Effect": "Allow",
            "Action": [
                "elasticloadbalancing:DeregisterInstancesFromLoadBalancer",
                "elasticloadbalancing:RegisterInstancesWithLoadBalancer"
            ],
            "Resource": [
                "*"
            ]
        },
        {
            "Sid": "Stmt1435902465000",
            "Effect": "Allow",
            "Action": [
                "ec2:CreateTags",
                "ec2:DeleteTags",
                "ec2:DescribeInstanceAttribute",
                "ec2:DescribeInstanceStatus",
                "ec2:DescribeInstances",
                "ec2:DescribeTags",
                "ec2:ModifyInstanceAttribute"
            ],
            "Resource": [
                "*"
            ]
        }
    ]
}

## How to run?
```
npm install
npm start

```

## Release History

## License
Copyright (c) 2015 AfterShip
Licensed under the MIT license.
