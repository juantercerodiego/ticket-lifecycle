<p align="center">
<img width="500" src="https://sjredwings-cdn.fxbrt.com/downloads/icons/os_ticket_sj_logo.png" alt="osTicket Logo"/>
</p>

<h1>osTicket: The Ticket Lifecycle & Incident Resolution</h1>

**Quick Note:** This lab demonstrates day-to-day help desk operations inside osTicket. If you want to see how I deployed and configured the osTicket server environment in Microsoft Azure first, check out that setup guide here: [Link to your osTicket Installation README].

This project walks through the complete end-to-end lifecycle of an IT support ticket. I simulate real-world help desk workflows—including user request creation, ticket triage, departmental assignment, agent communication, database verification, and final resolution.

<h2>Environments and Technologies Used</h2>

- **osTicket** (Open-Source Help Desk Ticketing System)
- **Microsoft Azure** (Virtual Machine Server Host)
- **Remote Desktop Connection (RDP)** (Remote Server Administration)
- **HeidiSQL** (MySQL Database Verification)
- **Web Browser** (Chrome / Edge)

<h2>Operating Systems Used</h2>

- **Windows 11 Pro** (Client & Administrative Workstation)

<h2>Prerequisites</h2>

- **Live osTicket Server:** An active instance hosted in Azure.
- **Agent/Admin Credentials:** Administrative access to handle triage and assignment.
- **Test End-User Account:** A simulated user account to submit support requests.

<br />

---

<h2>The Ticket Lifecycle (Step-by-Step)</h2>

<h2>Step 1: The Request (Ticket Creation)</h2>

Every IT issue begins with a request. A user logs into the support portal and submits a ticket detailing their issue (for example, "Password Reset Needed" or "Printer Offline"). The system automatically generates a unique Ticket ID so the issue can be tracked, prioritized, and audited.

<p align="center">
<img width="927" height="615" alt="Creating a Ticket in osTicket" src="https://github.com/user-attachments/assets/cabfd231-293a-4f8b-b349-04b105e4e304" />
</p>

<br />

---

<h2>Step 2: Triage & Assignment (The Hand-off)</h2>

Once submitted, the ticket enters the help desk queue for triage. The system routes the request to the appropriate department (e.g., IT Support, Systems Admin, or Billing). An Agent evaluates the priority level (Low, Medium, High, Emergency) based on business impact and claims ownership of the ticket to begin work.

<p align="center">
<img width="1299" height="800" alt="Assigning a Ticket to an Agent" src="https://github.com/user-attachments/assets/d2dab1b5-1f6b-4f64-b95a-fdaffd16b113" />
</p>

<br />

---

<h2>Step 3: Troubleshooting & Work in Progress</h2>

The assigned Agent communicates directly with the end-user through ticket replies, gathering details and attempting troubleshooting steps. Agents can also post **Internal Notes**—visible only to the IT team—to document diagnostic steps, system logs, or backend database updates checked via HeidiSQL.

<p align="center">
<img width="946" height="550" alt="Agent Working and Replying on a Ticket" src="https://github.com/user-attachments/assets/aebc1f03-8b13-4599-8a61-b2b0aae9603a" />
</p>

<br />

---

<h2>Step 4: Resolution & Ticket Closure</h2>

After verifying that the fix works and the user's issue is resolved, the Agent updates the status to **Resolved** or **Closed**. The user receives an automated email confirmation detailing the solution, and the ticket is permanently archived in the system for reporting and audit trail purposes.

<p align="center">
<img width="1415" height="700" alt="Closing and Resolving the Ticket" src="https://github.com/user-attachments/assets/c38cbf38-5817-45be-86fc-188a450cfb0a" />
</p>
