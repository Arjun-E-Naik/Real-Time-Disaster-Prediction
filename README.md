

### 🌪️ Weather Disaster Prediction & Response Agent

## AI-Driven Weather Monitoring | Disaster Detection | Human-in-the-Loop Verification | Automated Alert System

## 🚀 Overview

This project is an AI-powered autonomous agent system designed to detect potential weather-based disasters, analyze severity, generate emergency response plans, and optionally notify authorities via email.
It uses LLM agents, LangGraph, Weather APIs, and human-in-the-loop verification to make disaster management more intelligent, automated, and safe.

## 📌 Problem Statement

Extreme weather events such as floods, storms, heatwaves, and hurricanes are increasing globally.
Traditional monitoring systems often:

- Require manual interpretation

- Lack real-time proactive analysis

- Do not combine AI reasoning with real weather data

- Produce slow or inconsistent emergency responses

**Many local agencies do not have systems that can:**
- ✔ Automatically analyze weather conditions
- ✔ Predict possible disasters
- ✔ Provide actionable emergency plans
- ✔ Trigger alerts safely without false positives

**This project solves that gap using an AI agent workflow.**

## 🤖 Why Agents?

Agents are the right solution because they:

✅ Automate Multi-Step Reasoning

Each part of the pipeline—data fetching, analysis, decision routing—is handled by an agent with a dedicated responsibility.

✅ React to Real-Time Weather Data

The agent system adapts dynamically based on severity, disaster type, and conditions.

✅ Human-In-The-Loop Safety

Medium/low severity alerts require a human approval step to avoid unnecessary panic.

✅ Modular & Extensible

You can easily plug in more nodes like social media monitoring, satellite image analysis, or IoT sensor data.

✅ Autonomous Task Routing

LangGraph enables dynamic decision pathways such as:

High severity → emergency + direct alert

Flood/storm → public works

Low/medium → human approval required

# 🏗️ System Architecture

                ┌──────────────────────┐
                │   Start Workflow     │
                └─────────┬────────────┘
                          ↓
               ┌────────────────────────────┐
               │  Fetch Weather Data (API)  │
               └─────────┬──────────────────┘
                          ↓
           ┌────────────────────────┐
           │ Disaster Type Analysis │
           └─────────┬─────────────┘
                     ↓
        ┌────────────────────────────┐
        │      Data Logging          │
        └─────────┬──────────────────┘
                  ↓
       ┌───────────────────────────┐
       │   Route Based on Severity │─┬──────────┬─────────────┐
       └──────────────┬────────────┘ │           │             │
                      │              │           │             │
      ┌──────────────────────┐ ┌────────────┐ ┌────────────────────┐
      │ Emergency Response   │ │ Civil Def. │ │ Public Works Plan  │
      └─────────┬────────────┘ └─────┬──────┘ └─────────┬──────────┘
                ↓                    ↓                    ↓
      ┌──────────────────────┐ ┌──────────────────────────────────────┐
      │ Send Email (Auto)    │ │ Human Verification Required (Y/N)    │
      └─────────┬────────────┘ └─────────────────────┬──────────────┘
                ↓                                     ↓
       ┌────────────────┐                     ┌────────────────────┐
       │ Alert Sent     │                     │ Alert Not Sent     │
       └────────────────┘                     └────────────────────┘


**Email Example**

The agent automatically formats and sends alerts as text emails with:

**Weather details**

Disaster prediction

Severity

Emergency response plan

## **🛠️ The Build**

This system is built using:

- Core Technologies

- LangChain – LLM orchestration

- LangGraph – Agent state machine workflow

- Groq LLM (via ChatGroq) – Ultra-fast model inference

- WeatherAPI.com – Live weather feed

- Python – Main programming language

- LangSmith – Tracing, debugging, evaluation

- Gmail SMTP – Sending automated email alerts

**Key Features Implemented**

- ✔ Weather fetching module
- ✔ LLM-based disaster prediction
- ✔ Severity detection
- ✔ Routing logic using conditional edges
- ✔ Emergency / Public Works / Civil Defense agent nodes
- ✔ Human-in-the-loop verification node
- ✔ Email alert module
- ✔ Logging system
- ✔ StateGraph workflow for deterministic agent behavior

This is my simple approch to building agents using Langchain and Langgraph architecture.
