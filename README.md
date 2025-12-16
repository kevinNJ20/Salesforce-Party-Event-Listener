# Salesforce Party Event Listener

Listener d'événements Salesforce pour les Person Accounts et Contacts. Publie les événements vers Anypoint MQ Topics.

## Description

Cette application écoute les événements Salesforce concernant les Person Accounts et Contacts via des webhooks HTTP. Elle transforme ces événements et les publie vers les Topics Anypoint MQ correspondants.

## Endpoints Webhook

### POST /events/person-account
Reçoit les événements de Person Account depuis Salesforce et publie vers "Party Roles Topic".

### POST /events/contact
Reçoit les événements de Contact depuis Salesforce et publie vers "Parties Topic".

## Configuration

Voir README.md de Salesforce Financial Account Event Listener pour la configuration de base.

### Anypoint MQ Topics Requis

1. **Party Roles Topic** - pour les événements Person Account
2. **Parties Topic** - pour les événements Contact

### Queues Requises

1. **Party Roles Queue** → consomme depuis "Party Roles Topic"
2. **Parties Queue** → consomme depuis "Parties Topic"

## Port

- **Port HTTP**: 8084

