# s3admin-tooling
This is the documentation for s3admin-tooling API Service. The service provides APIs to interact with Amazon S3. The credentials for the Amazon S3 account is set in the S3AdminConfiguration.yml

## Deploying the service
### Build the application
'''
mvn clean package
'''
### Launching the application
The jar file of the application is present in ~/target folder. Use the following command to run launch the service
'''
sudo java -jar <s3admin-tooling-jar-file> server <path-to-S3AdminConfigurationFile.yml>
'''
