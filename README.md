# snapshotalyer
Demo project to manage AWS EC2 instance snapshots

## About
This project is a demo, and uses boto3 to manage AWS EC2 instance snapshots

## Configuring

analyser uses the configuration file created by the AWS Cli

## Running

'pipenv run python analyser/analyser.py'
<--project=Project>

*Command* is list, start, stops, snapshot
*subcommand* - depends on 
*project* is optional


## Add user with no permission
## configure AWS CLI for the user
aws configure --profile analyser
## install pipenv 3
install pipenv --three
## install Boto3
pipenv install boto3
## install ipython
pipenv install -d ipython
## run ipython inside pipenv
pipenv run ipython
## Import boto3
import boto3
## Create session
session = boto3.Session(profile_name='analyser')
## Connect to resource via session
ec2 = session.resource('ec2')
## perform scripts against your ec2 resource
 for i in ec2.instances.all():
     print(i)

## use history of codes you typed by using %history
%history

## install click module before you import it
pipenv install click
import click

## boto3 documentation
https://boto3.amazonaws.com/v1/documentation/api/latest/index.html

## Click documentations
https://click.palletsprojects.com/en/7.x/

## Packaging & creating distribution. Setup tools using the setup.py. We need to install setuptools. Users will be able to install your package using the setup.py
pipenv install -d setuptools
## we need to generat a wheel bdist_wheel command (an archive that let your Python code go places)
pipenv run python setup.py bdist_wheel
## install your dist
pip3 install dist/snapalyser
## Uninstall it so you can then install it using the S3 dist
pip3 uninstall snapshotalyser
