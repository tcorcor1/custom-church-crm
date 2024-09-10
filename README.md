# CRM Tool Built For Church Leaders/Admins

- [Summary](#summary)
- [Technology](#technology)
- [Demo](#demo)
- [Features](#features)

## Summary

A simple CRM built for church leadership teams that want to manage contacts/contact activity, meeting minutes/documents, events and announcements. Majority of components used are shadcn with exception of the grids. Although I love how the shadcn table looks, I went with MUI datagrid as it provided some features that I needed.

## Technology

- React 18.3.1 w/ TypeScript 4.9.5
- Shadcn & tailwind
- .NET 8 w/ .NET Identity
- EF Core 8.0.4
- PostgreSQL
- OData compliant
- Google SMTP & Google Places API
- AWS S3 for Document Management
- Serilog and Cloudwatch for logging/monitoring

## Demo

<div align="center">
  <img alt="Demo" src="/img/deacon-portal-demo_v1.gif">
</div>

## Features

### Dashboard

Implemented using <a href="https://recharts.org/en-US/" target="_blank">recharts</a> which is an amazing library and I highly recommend.

### Contacts

Implement using <a href="https://react-hook-form.com/" target="_blank">React Hook Form</a> and <a href="https://zod.dev/" target="_blank">zod</a> for validation. Upon creation of activities related to a contact, last activity date will be updated so users can tell if someone has been reached out to recently.

<div align="center">
  <img alt="Last Activity" src="/img/last-activity-date.png">
</div>

### Announcements

Users that have opted in to receive announcement notifications will be emailed when a new announcement is created or when a comment is added to an announcement they have commented/participated in already. This can all be managed in their notification preferences.

<div align="center">
  <img alt="Notification Preferences" src="/img/notification-preferences.png">
</div>

### Events

Implemented using <a href="https://fullcalendar.io/" target="_blank">FullCalendar</a> which is an amazing library and I highly recommend.

### Meeting Minutes

React Hook Form with Zod used to create & update meeting minutes. Also, supports document upload via S3.

### Documents

Document management implemented with AWS S3 using pre-signed URLs for download.

### Activities

Simple entity with a dynamic form that will change when selecting different activity types.

### Registration

Registration approvals were required for the site. This is mostly handled via identity, however, I added a registration approval step that is available to site admins

### Feedback

Used for bugs, general feedback and questions about the site.
