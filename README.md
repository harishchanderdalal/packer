# PACKER
Packer is use to create an AMI
- Json

## Template
```
{
  "buildes":[],
  "provisioners": [],
  "post-processors": []
}

## Example
```
{
    "buildes":[
      {
        "type": "amazon-ebs",
        "region": "us-west-1",
        "access_key": "foo",
        "secret_key": "bar",
        "source_ami": "ami_9abea4fb",
        "instance_type": "t2.micro",
        "ssh_username": "ubuntu",
        "ami_name": "MiddleTier-{{isotime | clean_ami_name}}",
        "ami_description": "Ami Designed WOW",
        "tags" :{
              "role": "My Ami"
        },
        "run_tags":{
                "role": "building"
        }
      }
    ]
}
```
