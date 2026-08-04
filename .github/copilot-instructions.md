## Copilot instructions for Lifecycle planning documentation

### Repository overview
Product: Lifecycle planning

*Lifecycle planning* is a feature in the NetApp Console that identifies storage assets with current or forecasted low capacity and recommends remediation options. The documented flows focus on capacity review, storage expansion guidance, cloud tiering, reminders, access, setup, support, and release-note history. Lifecycle planning is for on-premises ONTAP systems. 

### Repository structure
- `_include/` – Shared and reusable include content. This is currently a placeholder directory.
- `_whatsnew/` – Date-based release-note snippet files that are included into the published "What’s new" page.
- `get-started/` – Introductory and onboarding content for prerequisites, access, setup, login, and FAQ topics.
- `media/` – Shared images and visual assets referenced by the AsciiDoc pages.
- `release-notes/` – Release-note and limitations pages for Lifecycle planning.
- `support/` – Support and registration topics for getting help with the service.
- `use/` – Task content for reviewing capacity status, storage expansion, cloud tiering, and reminders.

### Product-specific context

- *NetApp Console* - The central management interface used to access Lifecycle planning.
- *Console agent* - The cloud-deployed connector used to connect the Console to your storage systems and data services.
- *Digital Advisor* - an alternate interface to access lifecycle planning (also called *Active IQ Digital Advisor*) 
- *Storage assets* & *clusters* - the primary objects evaluated by the service for current and forecasted capacity risk.
- *NetApp Cloud Tiering* - A NetApp service used to tier cold data. When lifecycle planning is identified as an option, it links to Cloud Tiering. 

### Typical user workflows

- *Initial setup* - This is part of the typical configuration for any Console user, which involves understanding prerequisites, creating a Console agent, and discovering storage in the NetApp Console. 

- *Capacity review & remediation* - Review the capacity of different storage assets then evaluate options. Actions can include expanding storage, tiering cold data, or reviewing best practices. If the user tiers cold data, this takes them to NetApp Cloud Tiering. 
