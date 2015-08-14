# s3admin-tooling
This is the documentation for s3admin-tooling API Service. The service provides APIs to interact with Amazon S3. The service needs the user to login using google sign in. The google token is validated by the service using the google client id. The Google client id and the credentials for the Amazon S3 account is specified in the S3AdminConfiguration.yml

## Dependencies
#### Database
The application needs a postgresql database. The database name, username, password is to be specified in the S3AdminConfiguration.yml file
```
database:

  driverClass: org.postgresql.Driver
  user: <database-username>
  password: <user-password>
  url: jdbc:postgresql://<hostname>:<port>/<database-name>
```
#### Custom Configurations
The Google client id and the credentials for Amazon S3 account is specified in the S3AdminConfiguration.yml file
```
customConfiguration:

  amazonS3AccessKey: <amazon-s3-access-key>
  amazonS3SecretKey: <amazon-s3-secret-key>
  googleClientId: <google-client-id>
  expiryTimeInMillis: 7200000
  dbCleanerWakeUpTime: 86400000
```

## Deploying the service
#### Build the application
```
mvn clean package
```
#### Launching the application
The jar file of the application is present in ~/target folder. Use the following command to run launch the service
```
sudo java -jar <s3admin-tooling-jar-file> server <path-to-S3AdminConfigurationFile.yml>
```
