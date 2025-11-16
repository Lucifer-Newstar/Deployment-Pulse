# Deployment Pulse

Deployment Pulse is a Zoho Cliq extension that brings deployment visibility directly into team conversations. It captures events from your CI/CD pipeline, processes them through Zoho Catalyst, and delivers structured notifications, interactive actions, and a compact dashboard — all inside Zoho Cliq.

Built fully on Zoho’s ecosystem, the system stays fast, lightweight, and easy to maintain.

* * *

## Features

· **Real-time deployment alerts** (start, success, failure)

· **Interactive cards** with rollback and log viewing

· **Deployment dashboard widget** with filters and search

· **Auto-refresh every 30 seconds**

· **Mobile-optimized design**

· **Clear status indicators & timestamps**

* * *

## How It Works

GitHub Actions → Webhook → Zoho Catalyst → Zoho Cliq Bot + Widget

· Webhook hits Catalyst

· Catalyst parses + stores deployment event

· Bot sends updates to Cliq

· Widget pulls data from Catalyst API for the dashboard

· Rollback/log actions are routed back to Catalyst via API

* * *

## API Overview

POST /webhook/deployment # receive GitHub events

GET /api/deployments # list all deployments

GET /api/deployments/:id # single deployment

GET /api/deployments/:id/logs # build/deploy logs

POST /actions/rollback/:id # create rollback PR

* * *

## Tech Stack

· **Zoho Catalyst** (Functions, Data Store, API Gateway)

· **Zoho Cliq** (Bot + Dashboard Widget)

· **GitHub Webhooks & API**

· **Node.js** for backend logic

* * *

## Quick Setup

1. Create a Zoho Catalyst project

2. Deploy functions + configure Data Store

3. Register a Zoho Cliq bot and link action endpoints

4. Add widget code to Cliq extension

5. Configure GitHub webhook to point to Catalyst

6. Test push → webhook → notification → dashboard

* * *

## Team

**Navin Jairam M** : DevOps & Full-Stack Engineering [navin.jairam@gmail.com](mailto:navin.jairam@gmail.com)

**Jegatheesan K** : Full-Stack Development & UI/UX [jegatheesanjegatheesan216@gmail.com](mailto:jegatheesanjegatheesan216@gmail.com)
