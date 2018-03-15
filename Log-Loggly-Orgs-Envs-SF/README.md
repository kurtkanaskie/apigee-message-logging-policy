## Configure
Set $HOME/.m2/settings.xml with profiles and passwords, for example:
```
<?xml version="1.0"?>
<settings xmlns="http://maven.apache.org/SETTINGS/1.0.0"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
	xsi:schemaLocation="http://maven.apache.org/SETTINGS/1.0.0 https://maven.apache.org/xsd/settings-1.0.0.xsd">
    <profiles>
        <profile>
            <id>training-test</id>
            <properties>
                <env.APIGEE_USERNAME>AdminUser@any.com</env.APIGEE_USERNAME>
                <env.APIGEE_PASSWORD>SueperSecre123</env.APIGEE_PASSWORD>
            </properties>
        </profile>
        <profile>
            <id>training-prod</id>
            <properties>
                <env.APIGEE_USERNAME>AdminUser@any.com</env.APIGEE_USERNAME>
                <env.APIGEE_PASSWORD>SueperSecre123</env.APIGEE_PASSWORD>
            </properties>
        </profile>
    </profiles>
</settings>
```

## Install
mvn install -P{profile-name}

