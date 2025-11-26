# Proposal Setup

## Proposal Title
**[HTLABS] Proteus: DynamicNFT Management Platform for Cardano**

## Proposer
- **Applicant:** HORIZON TECH LABS
- **Type:** Entity (Not Incorporated)

---

# Proposal Summary

## Budget Information
- **Requested Funds:** ₳120,000
- **USD Equivalent:** $50,400 (at 1 ADA = $0.42)

## Project Duration
- **Timeline:** 8 months

## Problem Statement
Dynamic NFTs have many applications such as tickets, certificates, and gaming assets, but adoption is difficult because the ecosystem lacks comprehensive tools for users to easily use or integrate.

## Solution Overview
Proteus simplifies dynamic NFT management. It provides a secure on-chain validator, a web dashboard, and a REST API to easily create, record, and update metadata without smart contract expertise.

## Supporting Documentation
- https://proteus.htlabs.xyz/
- https://github.com/htlabs-xyz/proteus
- https://drive.google.com/drive/folders/1Jkfv-8Y0pnhGAUWuKOtsR-c9tOlG-5PT?usp=sharing

## Project Dependencies
**Has Dependencies:** No

No Dependencies

## Open Source
**Is Open Source:** No (Open-Core Model)

We employ an Open-Core model where core smart contracts and validation logic are released open source via the MIT License, ensuring essential CIP-68 infrastructure remains free for the Cardano ecosystem. However, the backend API, frontend dashboards, and managed cloud services remain proprietary. This hybrid strategy balances community accessibility with sustainable platform operations through premium features and enterprise-grade support.

---

# Theme
- **Group:** Smart Contracts
- **Tag:** Smart Contracts

---

# Campaign Category

## Innovative Idea
What makes Proteus groundbreaking:

Proteus is the first comprehensive no-code platform dedicated to managing CIP-68 dynamic NFTs on Cardano.

**Current Ecosystem Gaps:**

- NMKR: Supports CIP-68 but lacks specialized dynamic NFT management features like rule-based automation, batch metadata updates, and template library
- JPG Store: Marketplace focused, no comprehensive minting and management tools for dynamic NFTs
- Saturn/Custom Solutions: Requires smart contract programming knowledge, no unified management interface or developer-friendly API

**Proteus Unique Innovations:**

- Rule-based automation: Creators configure automatic metadata updates based on events (time, transactions, oracle data) via a configuration interface
- Dual Interface: Intuitive, easy-to-use dashboard for creators + comprehensive REST API for developers
- CIP-68 Architecture: Built from the ground up for dynamic metadata, making assets mutable with certain conditions
- Supply Control System: Fine-grained control of mint/burn policies with time locks and condition-based issuance
- Batch Operations: Efficiently update large batches of NFTs in single transactions using intelligent batch processing algorithms
- Template Library: Pre-built templates for common use cases (game items, event tickets, membership levels, evolving art)

**Technical Differentiation:**

- Reusable smart contract architecture, reducing development costs for creators
- Off-chain indexing service enables fast metadata queries and real-time updates
- Multi-signature wallet support for team-managed collections
- On-chain activity logging for transparency and auditability

Innovation Impact: Proteus democratizes dynamic NFTs on Cardano, reducing development time from months (custom smart contracts) to hours (codeless configuration).

## Prototype/MVP
Proteus MVP: Fully functional dynamic NFT platform on Cardano Mainnet

Once the project is complete, the Proteus platform will be live on Cardano mainnet providing:

**Core Platform Features:**

- Intuitive Dashboard: Web interface for creating CIP-68 collections, minting NFTs (single or batch processing), and updating metadata without writing code
- Rules Automation Engine: Configuration-based automation that allows creators to set up conditional metadata updates (time-based, event-based, oracle-based)
- Developer API: Production REST API with comprehensive documentation and webhook integration
- Smart Contracts: Audited Plutus Validator deployed on mainnet, handling mint/burn/update operations with multi-signature support
- Sample Library: 10+ pre-built templates for common use cases (game items, event tickets, membership levels, evolving art)

**Demo & Accessibility:**

- Live Demo: "Proteus Platform" - working platform with all platform features (automatic updates, rules, metadata development)
- Public API Playground: Interactive sandbox allows developers to test API calls without deploying mainnet
- Video Tutorial: Comprehensive tutorial series showing non-developers creating dynamic NFT projects in under 30 minutes
- Open Source Repository: All smart contracts, API client examples, and documentation are publicly available on GitHub
- Community Access: Free plan allows immediate experimentation
- On-Chain Verification: Every feature is verifiable on the Cardano blockchain explorer - users can check smart contract code, track created NFTs, view transactions update metadata and independently test the platform's performance

**Testing & Validation:**

Before the mainnet launch, the platform will undergo:

- Over 50 beta testers creating real projects on the testnet
- 30-day public testnet period with integrated community feedback

## Performance Metrics
Success will be measured primarily through on-chain transaction activity verifiable via Cardano blockchain explorers. We'll track total transactions generated by Proteus smart contracts (minting, burning, metadata updates) recorded permanently on-chain with unique transaction hashes. NFT activity metrics include counting minted tokens, metadata update transactions, and burn operations - all identifiable through policy IDs generated by the platform. This data is tamper-proof and publicly auditable via CardanoScan or Blockfrost APIs.

Platform adoption will be measured by counting unique policy IDs created through Proteus, with each policy ID representing one deployed collection on-chain. Developer integration success will be tracked through API key registrations and monitoring which keys generate on-chain transactions, proving actual usage versus passive sign-ups. Smart contract interaction logs provide cryptographic proof of platform activity.

Ecosystem impact will be assessed by identifying and documenting new projects launching on Cardano using Proteus across verticals: GameFi projects, NFT ticketing implementations, DAO membership systems. Each project will be verifiable through their on-chain policy IDs and public announcements. Community engagement measured through GitHub repository metrics (stars, forks, contributors), Discord active member counts, and community-contributed templates in the marketplace.

All metrics will be published monthly via public dashboards displaying real-time blockchain data, compared against baseline Cardano NFT ecosystem activity. This ensures full transparency - anyone can independently verify our claims by querying the blockchain directly.

---

# Project & Solution

## Solution

### 📌 Context and Challenges
The Cardano NFT ecosystem faces a critical infrastructure gap limiting real-world adoption and competitive positioning. While Cardano introduced CIP-68 to enable dynamic NFTs with programmable, updatable metadata, the standard remains inaccessible to 95% of potential users due to:

**Technical Complexity Barrier**: Implementing CIP-68 requires deep knowledge of:

- Plutus smart contract development (Haskell/PlutusTx)
- UTXO model intricacies (reference NFT + user token architecture)
- On-chain datum encoding/decoding
- Transaction building with complex witnesses
- This expertise takes months to acquire, deterring non-blockchain developers

**Fragmented Tooling**: Existing solutions address pieces, not the whole:

- Mesh SDK: Low-level transaction builder (still requires coding)
- NMKR: Focused on static CIP-25
- Tangocrypto/Blockfrost: API infrastructure, but developers build everything else
- Custom Smart Contracts: Each project reinvents the wheel, no standardization

**CIP-25 Lock-in**: Most current NFT platforms only support static metadata:

- Metadata immutable post-mint
- Cannot register with token registry after minting
- Upgrading collections requires reminting (poor UX, environmental waste)
- Gaming/ticketing/membership use cases impossible

**Use Case Stagnation**: Without accessible dynamic NFTs, Cardano misses massive market opportunities:

- GameFi: Multi-billion dollar market requiring evolving in-game assets with dynamic metadata updates
- Event Ticketing: USD 39.8-85.35 billion market (2024) needing status updates (valid→used→expired) and real-time verification
- Membership/Loyalty: Tier upgrades, expiration dates, benefits tracking requiring programmable metadata
- Digital Identity: Soulbound tokens, credential updates, reputation scores with verifiable changes
- Evolving Art: Art that changes based on time, weather, market data, or other oracle inputs

**Consequence**: Developers choose Ethereum/Solana/Polygon where dynamic NFT infrastructure is mature (OpenSea, Thirdweb, Candy Machine v3), despite Cardano's superior architecture.

### 📌 Problem Summary
Cardano has CIP-68 standard for dynamic NFTs but lacks accessible tooling. Current solutions require months of Plutus development expertise, forcing majority of creators to either:

- Abandon dynamic NFT concepts
- Choose competing blockchains with mature tools
- Spend $100K+ on custom development

This infrastructure gap prevents Cardano from capturing multi-billion dollar gaming and ticketing (USD 39.8-85.35B in 2024) markets, despite having superior technology.

### 📌 Solutions
**Proteus: No-Code Platform + Developer API for Dynamic NFTs**

We deliver a comprehensive CIP-68 management platform with dual interfaces - visual dashboard for non-developers and REST API for technical teams.

**Architectural Decisions:**

Abstraction Layers:

- Layer 1: Smart Contracts (Plutus validators) - Reusable, audited, gas-optimized
- Layer 2: Off-Chain Workers - Handle metadata sync, event monitoring, automation
- Layer 3: API - Developer-friendly REST interfaces with comprehensive documentation
- Layer 4: Dashboard - Visual no-code interface for non-technical users

CIP-68 Native Design:

- Reference NFT + User Token architecture baked into every operation
- Automatic policy ID management and asset naming conventions
- Built-in datum schema validation preventing malformed metadata
- Optimized batching: group multiple NFT operations per transaction (within Cardano transaction size limits)

Rule-Based Automation Engine:

- Configuration-based rules: Define conditions and actions via dashboard or API
- Trigger sources: blockchain events, time schedules, external oracles, API calls
- Example: Schedule metadata updates for specific dates or wallet interactions
- Templates: Pre-configured rules for gaming upgrades, ticket lifecycles, membership tiers

Security-First:

- Multi-signature support for enterprise collections
- Granular permission system (minter, burner, updater roles)
- Audit trail: every metadata change logged on-chain with timestamp + signer
- Open-source smart contracts (community-auditable)
- Professional third-party security audit before mainnet

Developer Experience (DX):

- OpenAPI-compliant REST API (Swagger docs)
- Comprehensive API documentation with code examples
- Sandbox environment: test all features with testnet ADA (no risk)

Why This Approach:

Addressable market of 1,000+ Cardano projects versus < 50 with current tools. Easy onboarding creates network effects (more creators → richer ecosystem → attracts developers). Shared infrastructure reduces fragmentation and improves interoperability. Matches Ethereum/Solana tooling maturity while leveraging Cardano's cost/sustainability advantages.

### 📌 Content Summary
Proteus delivers four core components working together:

1. No-Code Dashboard for visual collection creation, batch minting, and metadata management without coding
2. Rule Automation Engine enabling automated metadata updates based on time, blockchain events, or oracle data through configuration interface
3. Developer API with REST endpoints and webhook integrations for programmatic access
4. Smart Contract Infrastructure providing reusable, audited Plutus validators handling CIP-68 mint/burn/update operations with multi-signature support

Target Users: Indie game developers building upgradeable in-game assets, NFT artists creating evolving art, event organizers implementing dynamic ticketing, DAO managers deploying membership systems, and enterprise teams building loyalty programs. Each vertical receives tailored templates, documentation, and integration support.

Engagement Strategy: Interactive onboarding tutorials, pre-built use case templates, comprehensive developer documentation, Discord community support, bi-weekly workshops, and public roadmap voting for feature prioritization.

Platform Features: Batch operations (process multiple NFTs per transaction within Cardano limits), template library (10+ pre-built patterns for gaming, tickets, memberships), real-time analytics dashboard, webhook notifications, sandbox testing environment, and open-source smart contracts for community auditability. All metadata changes logged on-chain for transparency and compliance requirements.

### 📌 Impact
Proteus directly enables Cardano ecosystem growth through measurable on-chain activity and market expansion. Platform success tracked via blockchain-verifiable metrics: transaction volume from Proteus smart contracts, unique policy IDs created (representing deployed collections), metadata update transactions proving dynamic capabilities usage, and total NFTs minted/burned. Platform analytics monitor dashboard registrations, API integration adoption, and template marketplace activity reported monthly.

Ecosystem impact manifests as:

- Competitive positioning - matching Ethereum/Solana tooling maturity while leveraging Cardano's cost advantages, enabling capture of multi-billion dollar gaming and ticketing (USD 39.8-85.35B) markets
- Developer attraction - removing technical barriers that cause projects to choose competing chains, providing enterprise-grade tooling comparable to Web2 development standards
- Transaction growth - dynamic NFT projects generate significantly more transactions than static collections through recurring metadata updates, creating sustainable on-chain activity
- Perception shift - moving Cardano from "research blockchain" to "production platform" status through proven real-world applications

Proteus fills critical infrastructure gap with unique value proposition: only CIP-68 specialized platform (no direct competition), dual interface serving both non-developers and technical teams, open architecture enabling ecosystem-wide integration, and adherence to Cardano native standards (CIP-68) for future-proofing. This transforms Cardano's technical superiority in dynamic NFTs into accessible tooling, enabling the next wave of NFT applications - gaming item upgrades, event ticketing systems, membership tier management, and evolving digital art.

---

## Impact

### 📌 In what way will the success of your project bring value to the Cardano Community?

**Non-Technical User Community Benefits:**

The no-code dashboard empowers non-technical users to create NFT collections, manage metadata, and burn assets through a simple interface without requiring programming knowledge or smart contract expertise. This accessibility directly benefits the Cardano community by:

- Increased Transaction Volume: Each user creating, updating, and managing dynamic NFTs generates on-chain transactions, contributing to network activity and validator rewards
- Wallet Growth: New creators joining Cardano to use Proteus means new wallet addresses and expanded user base
- Creator Economy: Artists, event organizers, and community managers can build on Cardano without technical barriers, attracting diverse use cases beyond current DeFi-focused demographics

**Developer Community Benefits:**

Providing open-source smart contracts, API client examples, and comprehensive documentation saves significant development time and costs for other projects:

- Time Savings: Companies deploy dynamic NFT applications faster (hours vs. months) by reusing audited smart contracts and integration patterns
- Cost Reduction: Eliminates need for custom Plutus development and security audits (saving $50K+ per project)
- Faster Time-to-Market: Projects launch on Cardano more quickly and simply, choosing Cardano over competing chains due to superior tooling availability

**Cardano Platform Sustainability:**

More projects deploying on Cardano generates more transactions, creating sustainable network activity:

- Transaction Fee Revenue: Recurring metadata updates (not just one-time mints) provide ongoing transaction fees
- Network Effects: Each successful project attracts similar projects, creating positive feedback loop
- Ecosystem Maturity: Demonstrates Cardano's production-readiness for dynamic NFT use cases (gaming, ticketing, memberships)

### 📌 How will you measure this impact?

**Quantitative Metrics:**

Open-source adoption and community engagement will be measured through:

- GitHub Repository Metrics: Number of package downloads, repository stars, forks, and contributors demonstrate developer interest and code reuse
- GitHub Issues & Feature Requests: Active issue discussions and feature requests indicate real-world usage and community engagement with the platform
- API Usage Statistics: Daily API call volume and unique API keys track how many projects actively integrate Proteus
- On-Chain Metrics: Transaction volume from Proteus smart contracts, unique policy IDs created, and metadata update transactions provide blockchain-verifiable proof of platform adoption
- Wallet Activity: Number of unique wallet addresses interacting with Proteus smart contracts shows ecosystem growth

**Qualitative Metrics:**

User satisfaction and community sentiment tracked through:

- Non-Technical User Feedback: Surveys and testimonials from creators using the no-code dashboard, measuring ease-of-use and feature completeness
- Developer Feedback: Input from technical teams integrating the API, focusing on documentation quality, integration simplicity, and time savings achieved
- Community Discussions: Sentiment analysis from Cardano Forum posts, Discord conversations, and social media mentions
- Case Studies: In-depth interviews with projects built on Proteus, documenting their experience and outcomes

### 📌 How will you share the outputs and opportunities that result from your project?

**GitHub Repository (Primary Channel):**

All project outputs will be shared through the open-source GitHub repository:

- Smart Contracts: Complete Plutus validator source code with deployment scripts and testing frameworks
- API Documentation: OpenAPI specifications, integration guides, and code examples
- Development Progress: Regular commits, pull requests, and release notes showing ongoing development
- Issue Tracking: Public issue tracker for bug reports, feature requests, and community discussions
- Documentation: Comprehensive guides, tutorials, and best practices published in repository wiki
- Milestone Updates: Progress reports for each Catalyst milestone published as GitHub releases

**Social Media Channels:**

Project updates, announcements, and opportunities shared via:

- Twitter/X: Development updates, feature announcements, and community highlights (tagged #ProteusOnCardano, #Cardano, #CIP68)
- Facebook: Community-focused updates, use case showcases, and creator spotlights
- Telegram: Real-time discussions, technical support, and community engagement with dedicated channel

**API Integration Updates:**

For developer community, technical updates delivered through:

- API Changelog: Versioned API documentation with breaking changes and new features clearly documented
- Webhook Notifications: Automated alerts for platform updates, new features, and maintenance windows
- Developer Newsletter: Monthly technical updates sent to registered API users

**Community Engagement:**

Regular interaction with Cardano ecosystem through:

- Cardano Forum: Monthly progress reports in Governance section with metrics and achievements
- Discord Servers: Active presence in Cardano Developers, NFT Guild, and Catalyst community servers
- Catalyst Town Halls: Participation in community calls to present progress and gather feedback
- Video Content: Tutorial series and feature demonstrations published on YouTube

**Opportunities Sharing:**

New opportunities resulting from the project communicated via:

- Partnership Announcements: Collaborations with other Cardano projects announced on all channels
- Integration Guides: Step-by-step guides for integrating Proteus with popular Cardano tools
- Hackathon Sponsorships: Proteus tracks at Cardano hackathons with prizes and mentorship
- Template Marketplace: Community-contributed templates and use cases shared in GitHub repository

All communication maintains transparency with links to on-chain evidence (transaction hashes, smart contract addresses) and GitHub commits, enabling independent verification of claims.

---

## Capability & Feasibility

Building on HTlabs' proven Cardano development track record, Proteus delivers production-ready CIP-68 infrastructure matching Web2 developer experience standards.

**Early User Interest & Market Validation**

Our Fund 12 CIP68 Generator has already attracted community interest:

- **GitHub Repository:** 15+ stars and growing community engagement
- **Community Inquiries:** Multiple Cardano developers have contacted HTlabs requesting dynamic NFT tooling
- **Cardano2VN Network:** Access to 500+ Vietnamese Cardano community members for beta testing
- **Previous Tool Usage:** cardano-tool.vercel.app (CIP25 minting) has served 200+ unique users, demonstrating demand for accessible NFT tools
- **Stake Pool Operators:** VILAI and HADA stake pools provide direct connection to delegator communities interested in NFT utilities

**Target early adopters identified through community engagement:**

- GameFi Projects: 3 Vietnamese game studios exploring Cardano NFT integration
- Event Organizers: Vietnam Cardano community events requiring dynamic ticketing
- NFT Artists: Local digital artists seeking evolving art capabilities

**Expertise and Experience**

HTlabs demonstrates deep Cardano expertise through multiple successful Catalyst projects and live production deployments:

**Key Projects:**

- Learning Management System: Production LMS at https://lms.cardano2vn.io
- Free Native Minting Tool (CIP25): Live at https://cardano-tool.vercel.app
- Complete Aiken Course: Fund 11 project - https://projectcatalyst.io/funds/11/cardano-open-ecosystem/the-complete-aiken-course-cardano-from-zero-to-expert
- Study Guide for Marlowe: Fund 10 project - https://projectcatalyst.io/funds/10/f10-startups-and-onboarding-for-students/study-guide-for-marlow
- Open Source CIP68 Generator: Fund 12 project - https://projectcatalyst.io/funds/12/cardano-use-cases-concept/open-source-dynamic-assets-tokennft-generator-cip68 (Direct predecessor)
    - GitHub Repository: https://github.com/htlabs-xyz/cip68generator
    - Status: Core CIP-68 validators completed and tested on preprod testnet
    - Prototype demonstrates: Basic mint/burn operations, reference NFT + user token architecture, metadata handling
    - Proteus builds upon this foundation by adding: Production-grade features, automation engine, developer API, no-code dashboard, template library, and enterprise capabilities

Additional projects include Cardano App Development Course, IoT Blockchain Templates, Dualtarget DeFi platform, Cardano Hackathons, and Vietnam NFT Exchange. Full portfolio: https://www.htlabs.xyz/projects

**Verification of Approach**

- Testnet Validation: Deploy platform and smart contracts on preprod testnet confirming performance (latency, throughput, gas optimization) and CIP-68 compliance. All contracts publicly verifiable on blockchain explorers.
- Open Beta Testing: 50-100 early adopters creating testnet collections, providing quantitative metrics (completion rates, error rates) and feedback to refine UX/documentation. Issues tracked via public GitHub.
- Progress Tracking: Transparent KPI reporting: API response <200ms, transaction success >99%, uptime >99.5%, user mint time <30min, beta completion >90%. Monthly reports on Cardano Forum/GitHub with on-chain evidence (TXIDs).

**Fund Management**

- Monthly Budget Reports: Detailed expenditure breakdowns by category (salaries, cloud services, audit) with line-item justification submitted to Catalyst monthly.
- Auditable Invoices: All third-party invoices (AWS, Cloudflare, Blockfrost, auditors) documented and archived for Catalyst review with full categorization.
- Milestone-Based Disbursements: Funds released only upon verified deliverables: KPI reports, on-chain evidence (TXID lists), GitHub releases, video demonstrations. Payment after Catalyst reviewer acceptance.

**Why We're Best Suited**

- Proven Catalyst Delivery: Successful completion of Fund 10, 11, 12, 13 projects demonstrates milestone management and accountability.
- CIP-68 Expertise: Fund 12 CIP68 Generator project means core challenges already solved—we're productizing proven technology, not experimenting.
- Full-Stack Capability: Portfolio spans smart contracts (Aiken, Marlowe, Plutus), web development (LMS, tools), and production infrastructure—delivering complete integrated systems.
- Community Trust: Transparent reporting, open-source contributions, and consistent delivery across multiple projects. Track record verifiable through live products and Catalyst history.

**Project Timeline Clarification**

The 8-month timeline features 6 major milestones with completion months listed. Work is continuous throughout:

- Month 1: Architecture & Planning (Milestone 1 completion)
- Month 2: Smart Contract Development (Milestone 2 completion)
- Months 3-4: Backend API Development (Milestone 3 completes Month 4)
- Months 5-6: Dashboard & User Interface (Milestone 4 completes Month 6)
- Month 7: Testing & Security Audit (Milestone 5 completion)
- Month 8: Mainnet Launch & Close-Out (Milestone 6 completion)

No gaps in development - milestones represent completion dates, not start dates. Team works continuously across all 8 months with overlapping workstreams.

---

# Milestones

## Milestone 1: Project Planning & Architecture Design
- **Delivery Month:** 1
- **Cost:** ₳12,000
- **Progress:** 10%

### Outputs
- Define system architecture and component design
- UI/UX design for dashboard and user interfaces
- Define team structure and working schedule
- Technical specification documentation
- Project management (organizing and controlling resources, tasks)

### Acceptance Criteria
- Architecture design document details system components and their interactions
- UI/UX design covers all major user flows (collection creation, minting, metadata updates)
- Team structure document defines roles, responsibilities, and working schedule
- Technical specification includes database schema, API structure, smart contract architecture
- All design documents reviewed and approved

### Evidence of Completion
- System architecture design document
- UI/UX design mockups and user flow diagrams
- Team structure and working schedule document
- Technical specification document
- Database schema and API structure documentation

---

## Milestone 2: Smart Contract Development
- **Delivery Month:** 2
- **Cost:** ₳24,000
- **Progress:** 30%

### Outputs
- Design CIP-68 smart contract specifications for minting, burning, metadata updates
- Develop Plutus/Aiken smart contracts with reference NFT and user token architecture
- Implement property-based testing and formal verification
- Deploy smart contracts on Cardano preprod testnet
- Smart contract security audit (internal - comprehensive review by blockchain security experts)
- Smart contract documentation and integration guides

### Acceptance Criteria
- Smart contracts deployed on preprod testnet with verified source code on CardanoScan
- 100% test coverage on critical contract paths using property-based testing
- Smart contracts handle mint, burn, and metadata update operations correctly
- Internal security audit completed with zero critical vulnerabilities
- Documentation includes contract specifications, datum/redeemer schemas, integration examples
- All test cases pass successfully on testnet

### Evidence of Completion
- Smart contract specification design document
- Testnet smart contract addresses (publicly verifiable on CardanoScan)
- GitHub repository with smart contract source code and comprehensive tests
- Internal security audit report
- Smart contract integration documentation

---

## Milestone 3: Backend API Development
- **Delivery Month:** 4
- **Cost:** ₳24,000
- **Progress:** 50%

### Outputs
- Backend architecture design and database schema
- REST API development (authentication, rate limiting, API key management)
- Transaction builder service integrating with smart contracts
- Metadata indexing service with IPFS/Arweave integration
- API documentation with OpenAPI specification
- API testing suite and performance optimization

### Acceptance Criteria
- REST API endpoints functional for mint, burn, update operations
- API documentation includes OpenAPI spec and interactive playground (Swagger UI)
- Authentication system supports API key management and rate limiting
- Transaction builder successfully creates and submits valid Cardano transactions
- Metadata indexing service syncs reference NFT updates within 2 blocks
- Load testing passes: Handle 100 concurrent requests without errors
- Code examples available for major languages (JavaScript, Python, curl)

### Evidence of Completion
- Backend architecture and database schema documentation
- GitHub repository with backend API source code
- API documentation site with interactive playground (live URL)
- Code example repository with multiple language samples
- Load test report showing performance metrics
- Video demonstration of API usage for NFT operations

---

## Milestone 4: Dashboard & User Interface
- **Delivery Month:** 6
- **Cost:** ₳30,000
- **Progress:** 70%

### Outputs
- Dashboard UI/UX design and prototyping
- Web dashboard development with collection creation wizard
- Batch minting interface (CSV upload, queue processing)
- Metadata update interface with preview functionality
- Rule configuration interface (automation builder)
- Template library: 10 pre-built use cases (gaming, tickets, membership, art)
- User authentication and project management interface

### Acceptance Criteria
- Dashboard accessible via web browser with mobile-responsive design
- Non-technical user can create collection and mint 50 NFTs in <30 minutes (user testing)
- Batch processing queue system handles large NFT collections efficiently
- Rule configuration interface supports conditional logic (AND, OR) and multiple triggers
- Templates work out-of-box: Deploy any template in <10 minutes
- User guide covers all dashboard features with step-by-step tutorials
- Platform uptime: 99% availability during testing period

### Evidence of Completion
- Public URL: (To Be Determined - live demo environment)
- GitHub release with complete dashboard source code (MIT License - fully open source)
- Video walkthrough showing non-developer creating dynamic NFT collection in under 30 minutes
- Template showcase: All 10+ templates functional on testnet with documentation
- Comprehensive user guide documentation covering all dashboard features
- UI/UX design documentation and design system specifications

---

## Milestone 5: Testing & Security Audit
- **Delivery Month:** 7
- **Cost:** ₳18,000
- **Progress:** 90%

### Outputs
- Deploy pilot version on preprod testnet
- Conduct open beta testing program (50-80 participants)
- Run bug bounty program
- Internal security audit by blockchain security experts
- Performance testing and optimization
- User acceptance testing (UAT)
- Address feedback and vulnerabilities

### Acceptance Criteria
- Pilot version deployed on preprod testnet with all features functional
- Beta testing program has minimum 50 participants creating real NFT collections
- Bug bounty program has minimum 10 participants with documented findings
- Internal security audit completed by experienced blockchain security experts with published report (no critical vulnerabilities identified)
- All UAT test cases pass successfully
- User feedback collected and critical issues addressed
- Performance benchmarks met: API <200ms response, >99% transaction success rate

### Evidence of Completion
- Testnet pilot URL (publicly accessible)
- Beta testing report with participant feedback and metrics
- Bug bounty program report with findings and resolutions
- Internal security audit report (PDF) with methodology and findings
- UAT test case documentation and results
- Performance benchmark report
- GitHub pull requests addressing identified issues

---

## Milestone 6: Mainnet Launch & Project Close-Out
- **Delivery Month:** 8
- **Cost:** ₳12,000
- **Progress:** 100%

### Outputs
- Deploy smart contracts on Cardano mainnet
- Launch production platform on mainnet
- Comprehensive documentation (user guides, developer docs, video tutorials)
- Community resources setup (Telegram, support portal, FAQ)
- Marketing campaign and launch announcements
- Project management (organizing and controlling resources, tasks)
- Final close-out report
- Final closeout video

### Acceptance Criteria
- Mainnet smart contracts deployed with zero critical vulnerabilities
- Production platform uptime: 99.5% over 30-day period
- Documentation completeness: 100% of features documented with examples
- Community launch: 100+ registered users within first month
- Launch announcements published on Cardano Forum, Essential Cardano, social media
- Final closeout report is publicly available
- Final closeout video is publicly available (3-5 minutes)
- Impact metrics tracked: transactions, users, projects, on-chain activity

### Evidence of Completion
- Mainnet smart contract addresses (CardanoScan verified)
- Production URL: (To Be Determined - publicly accessible)
- Documentation hub: (To Be Determined - live site)
- Video tutorials covering all platform features
- Community resource links (Discord, support portal)
- Launch announcement links (Cardano Forum, Essential Cardano, social media)
- Metrics dashboard URL: (To Be Determined - public real-time data)
- GitHub release: v1.0.0 tagged
- Link to final closeout report
- Link to final closeout video

---

# Final Pitch

## Team

### 📌 Nguyen Anh Tien – Project Manager | Blockchain Developer
**Role:** Oversees project delivery, product strategy, and blockchain architecture. Leads community engagement and stakeholder coordination for the Proteus platform.

**Experience:** 7+ years in Cardano/Crypto space since 2018. Founder of VILAI stake pool. Cardano Ambassador and Catalyst Funded Proposer. Graduate of Plutus Pioneer Program and Atala Prism Pioneer Program. Challenge Team member and Co-host for Eastern Town Hall

**Skills:** Project management, product ownership, Cardano ecosystem expertise, community leadership, stake pool operation.

**Contact:**
- Email: tienna@gmail.com
- Telegram: https://t.me/Tiennguyenanh

### 📌 Nguyen Van Hieu – Lead Blockchain Developer
**Role:** Develops and maintains core smart contract infrastructure, focusing on CIP-68 compliance and on-chain security. Provides technical leadership for blockchain integration.

**Experience:** Founder of HADA stake pool. Plutus Pioneer Program graduate. Lead Technical Support at multiple successful blockchain startups with deep expertise in Cardano development.

**Skills:** Plutus, Haskell, smart contract development, stake pool operation, technical support.

**Contact:**
- Email: nvhieu1978@gmail.com
- Telegram: https://t.me/nvhieu1978

### 📌 Phung Tien Dung – Fullstack Blockchain Developer
**Role:** Leads blockchain integration and smart contract development for CIP-68 dynamic NFT infrastructure, architecting reusable validators and ensuring secure, efficient on-chain operations for the Proteus platform.

**Experience:** 5+ years in software engineering, 2+ years in blockchain; expert in dApp development (Next.js) and smart contract writing (Aiken, Haskell). Contributed to multiple Catalyst-funded projects.

**Skills:** Node.js, Python, C/C++, Haskell, Aiken; proficient in Cardano blockchain development.

**Contact:**
- Email: tiendung0325@gmail.com
- Telegram: https://t.me/dijnie
- GitHub: https://github.com/dijnie

### 📌 Khanh Duy Nguyen – Blockchain Developer
**Role:** Develops backend API and frontend dashboard components, implementing wallet integration for seamless user onboarding and ensuring smooth platform functionality across all NFT management features.

**Experience:** Full-stack developer with expertise in building scalable web platforms. Specialized in blockchain application development and user-facing interfaces.

**Skills:** Backend and frontend development, web platform integration, wallet connectivity, API design.

**Contact:**
- Email: nguyenkhanh17112003@gmail.com
- Telegram: https://t.me/khanhnguyen1711

### 📌 Le Anh Quan – Full-Stack Developer | System Operator
**Role:** Manages infrastructure, DevOps pipelines, and system operations. Ensures platform reliability, scalability, and secure deployment across cloud environments.

**Experience:** Software engineering expert with 5+ years of backend experience at FPT Software. Extensive production system management and cloud deployment.

**Skills:** Java, Node.js, Python; proficient in system operations, DevOps management, and AWS deployment.

**Contact:**
- GitHub: https://github.com/anhquan0
- LinkedIn: https://www.linkedin.com/in/lenaquan306/

*More at: https://www.htlabs.xyz/members*

---

## Budget & Costs

**Total Requested: ₳120,000 ($50,400 USD at 1 ADA = $0.42)**

### Budget Breakdown

#### 1. Team & Development Costs — 60% | $30,240

**5-Person Development Team (8 months):**

| Role | Monthly | 8 Months |
|------|---------|----------|
| Project Manager/Blockchain Developer | $756 | $6,048 |
| Blockchain Developer | $756 | $6,048 |
| Full-Stack Developer/DevOps | $756 | $6,048 |
| UI/UX Designer | $756 | $6,048 |
| QA Engineer | $756 | $6,048 |
| **Total Team** | **$3,780** | **$30,240** |

*Note: At $756/month per person, this represents lean compensation demonstrating strong team co-investment in the Cardano ecosystem. Vietnam-based team rates are competitive globally while maintaining high quality output.*

**Development Deliverables Covered:**
- Smart Contract Development (CIP-68 validators, testing, optimization)
- Backend Development (REST API, database, off-chain workers, transaction builder)
- Frontend Development (Dashboard UI/UX, rule configuration, analytics)
- API Documentation (OpenAPI specs, integration guides, code examples)
- QA & Testing (Load testing, UAT, bug fixes, performance optimization)

#### 2. Infrastructure Costs — 15% | $7,560

**Hosting & Cloud Services (8 months): $4,032**

| Service | Monthly | 8 Months |
|---------|---------|----------|
| Cloud servers (AWS/GCP) | $252 | $2,016 |
| Database hosting (PostgreSQL) | $126 | $1,008 |
| CDN & storage (IPFS, Arweave) | $84 | $672 |
| Monitoring & logging (Datadog, Sentry) | $42 | $336 |

**Blockchain Infrastructure: $2,016**

| Service | Cost |
|---------|------|
| API services (Blockfrost, Koios) | $840 |
| IPFS services (Pinata, NFT.storage) | $1,176 |

**Development Tools: $1,512**

| Item | Cost |
|------|------|
| Software licenses (IDEs, design tools) | $504 |
| Third-party APIs (oracles, services) | $672 |
| Domain, SSL certificates, SaaS tools | $336 |

#### 3. Security & Audit — 10% | $5,040

**Internal Security Audit: $3,360**

| Activity | Cost |
|----------|------|
| Smart contract security review (formal verification) | $1,680 |
| API security analysis (penetration testing) | $840 |
| Infrastructure security review (DevOps) | $840 |

*Note: Internal audit by blockchain security experts. External third-party audit ($6,300-$12,600) may be pursued post-mainnet with platform revenue.*

**Security Tools & Testing: $1,680**

| Item | Cost |
|------|------|
| Penetration testing tools, scanners | $504 |
| Bug bounty program | $840 |
| Security monitoring (WAF, DDoS) | $336 |

#### 4. Operations & Community — 15% | $7,560

**Project Management: $2,016**

| Item | Cost |
|------|------|
| Project coordination tools (Jira, Notion) | $168 |
| Legal & compliance consultation | $840 |
| Accounting & financial reporting | $504 |
| Contingency buffer | $504 |

**Marketing & Community: $2,856**

| Item | Cost |
|------|------|
| Website development (landing, docs) | $1,008 |
| Educational content (videos, tutorials) | $840 |
| Community engagement (Discord, AMAs) | $504 |
| Launch marketing (announcements, PR) | $504 |

**Documentation & Support: $1,680**

| Item | Cost |
|------|------|
| Technical writing (guides, API docs) | $1,008 |
| Video tutorials production | $504 |
| Support infrastructure (ticketing) | $168 |

**Project Close-Out: $1,008**

| Item | Cost |
|------|------|
| Close-Out Report preparation | $504 |
| Close-Out Video production | $504 |

### Budget Summary

| Category | Allocation | USD |
|----------|------------|-----|
| Team & Development | 60% | $30,240 |
| Infrastructure | 15% | $7,560 |
| Security & Audit | 10% | $5,040 |
| Operations & Community | 15% | $7,560 |
| **TOTAL** | **100%** | **$50,400** |

### Milestone-Based Payment Schedule

| Milestone | Month | Deliverable | USD |
|-----------|-------|-------------|-----|
| M1 | 1 | Planning & Architecture Design | $5,040 |
| M2 | 2 | Smart Contract Development | $10,080 |
| M3 | 4 | Backend API Development | $10,080 |
| M4 | 6 | Dashboard & User Interface | $12,600 |
| M5 | 7 | Testing & Security Audit | $7,560 |
| M6 | 8 | Mainnet Launch & Close-Out | $5,040 |
| **Total** | | | **$50,400** |

---

## Value for Money

The value of the Proteus Dynamic NFT Platform project, budgeted at ₳120,000 ($50,400 at 1₳ = $0.42), is demonstrated by these key benefits for Cardano:

**Increased user adoption:** No-code dashboard and intuitive interface draw non-technical creators (artists, event organizers, game developers) to Cardano, expanding the ecosystem's user base.

**Promotes CIP-68 innovation:** Showcases CIP-68's dynamic NFT capabilities, driving widespread adoption of updatable metadata standard across GameFi, ticketing, and membership applications.

**Increased transactions:** Dynamic NFT operations (minting, metadata updates, burns) generate recurring on-chain activity, enhancing ecosystem engagement beyond one-time static NFT mints.

**Boosted NFT ecosystem:** Production-ready platform with templates and APIs inspires developers with accessible CIP-68 implementation model, strengthening Cardano's competitiveness in multi-billion dollar GameFi and ticketing (USD 39.8-85.35B) markets.

**Enhanced NFT functionality:** Transparent, verifiable dynamic NFTs with updatable metadata streamline asset management without third-party reliance or custom smart contract development.

**Cost Justification:**

The 8-month project with a 5-person team (HTlabs) averages $756/month per person. This lean compensation demonstrates strong team co-investment in the Cardano ecosystem. Budget covers team salaries ($30,240), AWS/Cloudflare/Blockfrost infrastructure ($7,560), security audit ($5,040), and operations/community engagement ($7,560).

**Cost Comparison:**
- Custom CIP-68 development by external agency: $80,000-$150,000
- Proteus delivers complete platform: $50,400 (66% savings minimum)
- Per-project savings for ecosystem: $50,000+ per project using Proteus instead of custom development

**Value Proposition:**

The project delivers a production-ready CIP-68 platform, open-source smart contracts, comprehensive documentation (user guides, API docs, video tutorials), and community engagement (beta testing, Discord support, workshops), driving Cardano NFT ecosystem growth and CIP-68 standard adoption. Monthly Catalyst reports ensuring compliance with Fund Rules.

---

# Self Assessment Checklist

| Criteria | Status |
|----------|--------|
| Foundational Work | ✅ |
| Ecosystem Value | ✅ |
| Builder Credentials | ✅ |
| Catalyst Standing | ✅ |
| Problem/Use Case | ✅ |
| Tangible Prototype | ✅ |
| Technical Approach | ✅ |
| Realistic Scope | ✅ |
| Community Engagement | ✅ |
| Budget Compliance | ✅ |

---

# Agreements

## Ongoing Projects
**Has Ongoing Projects:** No

## Consent Confirmation
**Terms and Conditions:** ✅ Accepted
