# Day 4 – Hour 2: Wazuh Architecture

## Main Components

### Endpoint
Device being monitored.

### Agent
Collects logs and sends them to the Manager.

### Manager
Analyzes logs and generates alerts.

### Indexer
Stores logs and alerts for searching.

### Dashboard
Displays alerts and security information.

## Log Flow

Endpoint → Agent → Manager → Indexer → Dashboard

## Key Insight

The Manager performs detection while the Dashboard provides visibility for SOC analysts.

## SOC Relevance

Understanding the architecture helps analysts trace alerts back to their source and investigate incidents efficiently.
