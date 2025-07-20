# Architecture Guide

This document outlines the architectural principles of the Breaker Breaker project, focusing on the distinction between Packages, Features, and Modules.

## The Core Concepts

Think of the project like building a car:

1.  **Package (`packages/`): The Major Components of the Car**
    *   **What it is:** A high-level, deployable, and largely independent part of the system. It's a major "chunk" of the application.
    *   **Our Project:** We have `backend`, `webapp`, and `mobile-app`. Each of these is a separate "package" that can be built, tested, and deployed on its own.
    *   **Analogy:** The **engine**, the **chassis**, and the **infotainment system**. They are all distinct parts that come together to make the car work, but you can develop or replace one without completely rebuilding the others.

2.  **Feature (`features/`): What the User Can Do with the Car**
    *   **What it is:** A specific piece of user-facing functionality. It describes a complete user story or a goal the user can achieve.
    *   **Our Project:** `feature-user-authentication.md` describes the login/registration flow. `feature-cb-radio.md` describes how a user interacts with the communication tools.
    *   **Analogy:** "Cruise Control," "Air Conditioning," or "Playing Music." These are the features a driver uses. They don't care *how* the A/C works, just that they can turn it on and get cold air.

3.  **Module (`modules/`): The Internal Systems That Power the Features**
    *   **What it is:** A logical grouping of code that provides a specific, self-contained capability. Modules are the building blocks that developers use to implement features. They are not something the end-user directly interacts with.
    *   **Our Project:** We have a `communication.md` module. This module contains the underlying logic for sending messages, handling PTT sessions, etc. This single module can be used to power multiple features, like "Private Chat" and "Fleet-wide Broadcasts."
    *   **Analogy:** The **electrical system**, the **engine control unit (ECU)**, or the **cooling system**. A driver doesn't "use" the electrical system directly, but it powers the "Play Music" and "Air Conditioning" features.

## Relationship Summary

> **Packages** are the major deployable parts of our application. They are built from **Modules**, which provide the core logic. This logic is then used to implement user-facing **Features**.
