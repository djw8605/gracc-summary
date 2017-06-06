GRACC Summary Daemon
====================

This daemon periodically request the summarization of GRACC records

[![Build Status](https://travis-ci.org/opensciencegrid/gracc-summary.svg?branch=master)](https://travis-ci.org/opensciencegrid/gracc-summary)

## Installing

It is easy to install the GRACC Summary Daemon with virtualenv

    virtualenv gracc-test
    . gracc-test/bin/activate
    pip install -r requirements.txt
    python setup.py install


## Running Re-Summarization

If gracc-summary is installed on the node:

    graccsummarizer "amqps://username:password@rabbitmq:5671/gracc" --destination_exchange gracc.osg.summary --destination_key gracc.osg.summary --type=summary 2016-11-01 2017-02-01
    
If you are using the docker installation, the command will be:

    sudo docker run opensciencegrid/gracc-summary /usr/bin/graccsummarizer "amqps://gracc:%3C9zLh.qC%24CVme6L%5B@event.grid.iu.edu:5671/gracc" --destination_exchange gracc.osg.summary --destination_key gracc.osg.summary --type=summary 2016-11-01 2017-02-01


## Docker Installation

A docker image with gracc-summary installed in available as opensciencegrid/gracc-summary.  