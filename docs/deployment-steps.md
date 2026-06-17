# Deployment Steps

## Launch EC2 Instances

Created 3 Amazon Linux EC2 instances.

## Install Apache

```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl enable httpd
sudo systemctl start httpd
```

## Create Web Pages

Instance 1:

```html
<h1>This is Instance 1</h1>
```

Instance 2:

```html
<h1>This is Instance 2</h1>
```

Instance 3:

```html
<h1>This is Instance 3</h1>
```

## Create Target Group

- Protocol: HTTP
- Port: 80

## Register Instances

Added all 3 EC2 instances.

## Create Application Load Balancer

- Internet-facing
- Listener: HTTP 80

## Attach Target Group

Connected target group to ALB.

## Verify

Opened ALB DNS name and confirmed traffic routing.