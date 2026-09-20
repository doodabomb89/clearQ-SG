ClearQ SG

A digital queue management system for GP clinics in Singapore, letting patients check their position in line remotely instead of waiting physically on site. Built under my startup VeenaTech.

Overview

Clinics in Singapore often still rely on physical queue numbers, meaning patients have to wait on site to track their turn. ClearQ solves this by having patients scan a QR code to register into the queue and track their status from their phone, while clinic staff manage everything from a dedicated receptionist dashboard. I've reached out to over 30 clinics directly and currently have 3 lined up to purchase the product once the backend is connected. This repo contains a fully interactive HTML/CSS/JS prototype simulating the entire patient and staff experience, built to validate the product with clinics ahead of a full backend build.

My Role

Founder and sole builder. Designed and built the entire prototype, covering the patient registration flow, live queue view, and staff dashboard, and used it directly in sales conversations and demos with over 30 clinics.

Current Status

This repo is a self-contained, fully interactive prototype with no backend yet. It's built to demonstrate the product experience end to end while I wait on API access from clinic CMS providers, starting with Plato Medical, to connect ClearQ to real clinic booking data. The planned production stack is Supabase, Vercel, and Twilio.

What's in the Prototype
Patient Registration (QR 1): simulates a patient scanning the clinic's QR code, being redirected through the clinic's existing CMS, modeled here on Plato Medical, to select a visit purpose, book a slot, and receive a queue number, all without ClearQ ever directly handling the patient's personal data
Queue Status (Patient View): a live view showing the patient's queue number, how many people are ahead of them, and an estimated wait time
Receptionist Dashboard (Staff Only): lets staff see the full queue, add walk in patients manually, mark patients as arrived or a no show, and toggle clinic status between open, lunch, and closed
Returning patient recognition: simulates looking up a patient by phone number against existing clinic records to speed up registration
Design Approach

ClearQ is designed to sit alongside a clinic's existing CMS rather than replace it. In this prototype, the clinic's CMS, represented here as Plato Medical, owns the patient booking data, and ClearQ receives a queue number and name back through what would be a webhook in production. This keeps ClearQ lightweight to adopt for clinics that already have a booking system in place.

Tech Stack (Prototype)

Plain HTML, CSS, and JavaScript, self contained in a single file for easy demoing.

Planned Tech Stack (Production)
Backend and database: Supabase
Hosting: Vercel
Notifications: Twilio
Screenshots / Demo

Add screenshots of the patient registration flow, queue view, and dashboard here.

What I Learned

Building a fully interactive prototype before writing any backend code let me validate the actual patient and staff experience with real clinics before committing to infrastructure. Reaching out to over 30 clinics also taught me how much a small, unproven vendor has to work to earn trust against established systems, many were hesitant even to take a meeting. Landing 3 clinics willing to commit to purchasing once the backend is live showed me that a strong prototype and a clear pitch can overcome that hesitation, even before the product is fully built.
