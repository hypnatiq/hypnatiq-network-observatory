# Hypnatiq Network Observatory

HypNO is a personal Windows endpoint and network-investigation project that demonstrates how I approach Windows endpoint research, network troubleshooting, evidence validation, application risk, controlled testing, and technical documentation.

## What this demonstrates professionally

This project brings together the parts of endpoint and network support that I want to keep building on: process attribution, TCP and UDP review, packet evidence, DNS and destination context, publisher and signature checks, Windows Firewall decisions, repeatable testing, and clear escalation notes.

I am not presenting HypNO as employer production ownership or as a replacement for antivirus. I am showing how I take an unfamiliar connection, organize the evidence, state what remains unknown, and document the next safe action.

## Why I created HypNO

The project began while I was learning how applications communicate through inbound and outbound network connections on Windows.

I worked with Windows Firewall, Simplewall, endpoint-protection tools, packet captures, and IP-intelligence services to investigate unfamiliar activity. I learned that seeing an IP address, firewall rule, or security alert was rarely enough to understand what had actually happened.

I still needed to answer several connected questions:

1. Which process or application initiated the connection?
2. What was observed directly on the computer?
3. What did external intelligence sources report?
4. Is the activity expected, suspicious, known malicious, or still unresolved?
5. What action does the available evidence justify?

HypNO grew from the workflow I developed to answer those questions consistently.

## What HypNO is

HypNO is a Windows network-observation and investigation project. It connects live TCP and UDP activity and imported PCAP or PCAPNG captures to the responsible process, service, executable, publisher, and digital signature when Windows can provide that identity.

Optional integrations add context from sources such as:

- VirusTotal
- AbuseIPDB
- GreyNoise
- ThreatFox
- MaxMind GeoLite
- TShark

HypNO keeps locally observed evidence separate from third-party provider reports. It uses the combined evidence to help classify activity as expected, suspicious, known malicious, or unresolved when the available evidence supports that conclusion.

The workflow is designed to help a user understand what happened before making a reviewed Allow or Block decision through Windows Firewall.

## What HypNO helps a user do

- Import PCAP and PCAPNG captures and review live TCP and UDP activity
- Connect supported activity to the responsible process, service, executable, publisher, and digital signature
- Organize packet and destination evidence with TShark and MaxMind GeoLite
- Add optional context from VirusTotal, AbuseIPDB, GreyNoise, and ThreatFox
- Separate confirmed local facts from third-party provider results
- Classify activity only as far as the available evidence supports
- Review an Allow or Block decision before a reversible Windows Firewall rule is written
- Record what changed, whether the response worked, and how to recover it

## Relationship to antivirus

HypNO complements antivirus rather than replacing it.

Antivirus products focus on file, behavior, and endpoint protection. HypNO focuses on investigating an application's network activity:

- What destination did it contact?
- Which process caused the connection?
- What evidence exists locally?
- What do external intelligence sources report?
- What remains uncertain?
- What network response should be reviewed?

A confirmed provider match can support a malicious or suspicious classification. A clean, unknown, or missing result is not treated as proof that an application or destination is safe.

## How the evidence is presented

HypNO keeps three things distinct:

1. **Observed locally:** the process, executable, connection endpoints, timestamps, signature details, and Windows-reported state.
2. **Reported by an external source:** the result returned by a selected intelligence or reputation provider at that time.
3. **Still unresolved:** anything the available evidence cannot safely establish.

HypNO shows the source and limits of each result so the user can make a reviewed decision instead of relying on one label.

## What is included

- Public product and architecture documentation
- An explanation of the investigation workflow and safety boundaries
- Comparison and capability pages
- Seven selected interface screenshots that do not expose machine paths, network addresses, installed application details, or firewall-rule information
- Clear labels for what was observed, what information is optional, what action is proposed, and what was actually verified

## What remains private

- The Windows application and service source code
- Private correlation, decision-support, and firewall-rule implementation details
- Credentials, API keys, tokens, signing material, customer data, and captured personal traffic
- Local databases, machine paths, private endpoints, and test captures
- Any material that could expose a real system or enable an unsafe security-control change without review

This public repository explains the problem, product direction, safety model, and selected interface design. It is not a source release.

## Current status

The repository includes selected screenshots of the HypNO 0.80 development interface and the direction of the product. They do not prove that every screen is active in an installed build, that every connection can be attributed, that an online lookup proves safety, or that the application is production-ready.

The public project name is **Hypnatiq Network Observatory**. The Windows application is called **HypNO**. They are two names for the same project, not separate products.

## Where to start

1. Read [docs/architecture.md](https://github.com/hypnatiq/hypnatiq-network-observatory/blob/main/docs/architecture.md) to follow the evidence flow.
2. Read [docs/privacy-safety-and-limitations.md](https://github.com/hypnatiq/hypnatiq-network-observatory/blob/main/docs/privacy-safety-and-limitations.md) for the limits and safety model.
3. Review [screenshots/README.md](https://github.com/hypnatiq/hypnatiq-network-observatory/blob/main/screenshots/README.md) and the seven selected screenshots.
4. Read [docs/publication-review.md](https://github.com/hypnatiq/hypnatiq-network-observatory/blob/main/docs/publication-review.md) before adding source material or captures.

## Portfolio context

This project represents how I investigate unfamiliar technical problems, validate evidence, document uncertainty, test safely, and convert research into a repeatable support workflow.

The public repository documents the product direction, investigation model, safety boundaries, and selected interface examples. Private source code, internal decision logic, provider credentials, and sensitive machine evidence are intentionally excluded.

It is not presented as prior employer production ownership.

Copyright 2026 Hanzley Philippeaux. See [LICENSE.md](https://github.com/hypnatiq/hypnatiq-network-observatory/blob/main/LICENSE.md) and [SECURITY.md](https://github.com/hypnatiq/hypnatiq-network-observatory/blob/main/SECURITY.md).
