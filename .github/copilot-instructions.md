## Copilot instructions for Lifecycle planning documentation

### Repository overview
Product: Lifecycle planning

*Lifecycle planning* is a feature in *NetApp Console* that identifies storage assets with current or forecasted low capacity and recommends remediation options. The documented flows focus on capacity review, storage expansion guidance for *AFF* systems, cloud tiering, reminders, access, setup, support, and release-note history.

### Repository structure
- `_include/` – Special-purpose folder for shared include content; currently only a placeholder README keeps the directory in the repository.
- `_whatsnew/` – Date-based release-note snippet files that are included into the published “What’s new” page.
- `get-started/` – Introductory and onboarding content for prerequisites, access, setup, login, and FAQ topics.
- `media/` – Shared images and visual assets referenced by the AsciiDoc pages.
- `release-notes/` – Release-note and limitations pages for Lifecycle planning.
- `support/` – Support and registration topics for getting help with the service.
- `use/` – Task content for reviewing capacity status, storage expansion, cloud tiering, and reminders.

### Product-specific context
**Architecture and components:**
- *Lifecycle planning* is accessed through *NetApp Console* and can also be reached from *Digital Advisor* through the planning widget path documented in the repo.
- A *Console agent* provides connectivity and credentials to *NetApp ONTAP* systems; some workflows can prompt users to deploy the agent during remediation.
- *Cluster discovery* happens in the Console before the service can work with an ONTAP cluster; discovery can be completed ahead of time or during a remediation flow.
- When a recommendation is to tier cold data, Lifecycle planning hands the workflow off to *NetApp Cloud Tiering* for the actual tiering setup.

**Key concepts:**
- *Storage assets* and *clusters* are the primary objects evaluated by the service for current and forecasted capacity risk.
- *Capacity planning* identifies assets with low capacity now or in the forecast window and uses AI-based data-growth forecasting to support planning decisions.
- *Evaluate Storage Options* is the decision point where users choose an action for an asset, such as *Storage Expansion*, *Tier cold data*, *Best Practices*, or *No action needed*.
- *Storage Expansion* is the capacity-growth workflow for *AFF* systems and can produce add-on storage recommendations or alternate-option requests.
- *Reminders* let users defer action and resurface the low-capacity risk after a selected interval.

**Naming conventions and terminology:**
- Use *Lifecycle planning* as the current product/feature name; older release-note content references *BlueXP economic efficiency* as the previous name.
- Use *NetApp Console* for the management interface, not generic “portal” wording.
- Use *Console agent* and *discover the cluster* for prerequisite connectivity steps; these are explicit setup actions in the repo.
- Use *forecasted capacity*, *low-capacity resources*, *tier cold data*, and *Storage Expansion* exactly as documented task terminology.
- *Digital Advisor* is also referred to as *Active IQ Digital Advisor* in the intro content.

### Typical user workflows
**Initial setup:** Review prerequisites → create a *Console agent* → discover the ONTAP cluster in *NetApp Console* → open *Lifecycle planning*

**Capacity remediation:** Log in to *NetApp Console* → review low-capacity assets → open an asset and select *Evaluate Storage Options* → choose *Storage Expansion*, *Tier cold data*, *Best Practices*, or *No action needed*

**Cold-data tiering:** Open an asset recommendation → select *Tier Cold Data* → deploy a *Console agent* if needed → discover the cluster if needed → continue in *NetApp Cloud Tiering* to configure tiering

**Storage expansion:** Open an asset → select *Storage Expansion* → review forecasted or custom growth inputs → review recommended add-on storage or request alternate options → confirm and submit the request
