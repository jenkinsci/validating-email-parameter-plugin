Jenkins Validating Email Parameter Plugin
==============

Plugin;
- performs e-mail validation
- prevents sending e-mails except the specified domain.
- prevents typo

## Parameter Definition;

![](./src/main/resources/io/jenkins/plugins/image/p1.png)

- Default Value  : Specifies the default value of the field, which allows the user to save typing the actual value.

- Domain         : Permitted domain name for sending mail.

![](./src/main/resources/io/jenkins/plugins/image/p2.png)

## Validation;

<img src="./src/main/resources/io/jenkins/plugins/image/p3.png" width="550" height="250">

<img src="./src/main/resources/io/jenkins/plugins/image/p4.png" width="550" height="250">

<img src="./src/main/resources/io/jenkins/plugins/image/p8.png" width="550" height="250">

<img src="./src/main/resources/io/jenkins/plugins/image/p6.png" width="550" height="250">

### External Email : If checked, Sending mail is allowed outside the set domain name.

<img src="./src/main/resources/io/jenkins/plugins/image/p5.png" width="550" height="250">

### External Email : ### false

<img src="./src/main/resources/io/jenkins/plugins/image/p7.png" width="550" height="250">

## Build;

- Invalid Email;

![](./src/main/resources/io/jenkins/plugins/image/p9.png)

- Valid Email;

![](./src/main/resources/io/jenkins/plugins/image/p10.png)

## You can copy that code directly into the pipeline block in your Jenkinsfile;

```node

parameters {
  validation defaultValue: 'sezai.can team.mail', description: 'Email Address', domain: 'sahibinden.com', externalEmail: true, name: 'EMAIL'
}


```

![](./src/main/resources/io/jenkins/plugins/image/p11.png)
