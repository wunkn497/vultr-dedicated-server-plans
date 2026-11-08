# Vultr Dedicated Server: Bare Metal vs Dedicated Cloud, What the Plans Cost, and When a $79 Dallas Box Fits Better (Full Plan Table)

Vultr sells dedicated servers under two product names, and the two behave very differently. **Bare Metal** is an entire physical machine with no virtualization layer, offered in 7 of Vultr's 15 regions on a burstable 10GbE connection. **Dedicated Cloud** rents 25%, 50%, 75% or 100% of a machine in 4 regions (New Jersey, Chicago, Silicon Valley, Tokyo), capped at 8 dedicated vCPUs on a 1GbE uplink. Both bill by the hour with no long-term contract. Neither one refunds you when you cancel, and a stopped instance keeps charging until you destroy it.

Plan tables published by review sites put Vultr's dedicated lines between **$60 and $240 per month**, with Bare Metal listed at **$120/month**. If what you actually need is a plain US box with a lot of RAM, NVMe storage and transfer allowance, SpinServers in Dallas starts at **$79/month** for 4 cores/8 threads, 32GB ECC memory, 1TB NVMe and 30TB of monthly traffic.

> **Quick pick**
> - Whole physical machine, a European or Asian region, or hourly create-and-destroy through an API: Vultr Bare Metal, listed at $120/month.
> - Dedicated vCPUs without paying for an entire server: Vultr Dedicated Cloud, listed from $60/month.
> - Maximum cores, memory and bandwidth per dollar, US locations only: SpinServers Dallas from $79/month.
>
> 👉 [See the current Dallas dedicated server configurations at SpinServers](https://bit.ly/Spinservers)

## What Vultr's dedicated server lineup actually contains

Two product lines, two different sets of limits:

| Product | Locations | Network | Smallest unit you can rent |
| --- | --- | --- | --- |
| Bare Metal | Chicago, Los Angeles, Miami, Silicon Valley, Amsterdam, Singapore, New Jersey (7 of 15 regions) | Burstable 10GbE per instance | Entire server |
| Dedicated Cloud | New Jersey, Chicago, Silicon Valley, Tokyo | 1GbE uplink, up to 40,000GB transfer | 25% of a server |

The published plan listings look like this:

| Plan | Specs as listed | Monthly | Hourly |
| --- | --- | --- | --- |
| Dedicated Instances 1 | 120GB SSD, 10TB transfer, 2 CPU, 8GB RAM | $60 | $0.089 |
| Dedicated Instances 2 | 2×120GB SSD, 20TB, 4 CPU, 16GB | $120 | $0.179 |
| Dedicated Instances 3 | 3×120GB SSD, 30TB, 6 CPU, 24GB | $180 | $0.268 |
| Dedicated Instances 4 | 4×120GB SSD, 40TB, 8 CPU, 32GB | $240 | $0.357 |
| Bare Metal | 2×240GB SSD, 5TB, 8 CPU, 32GB | $120 | $0.179 |

A warning about those numbers: they come from third-party plan tables, one of which was published in 2016 and another with no date at all. Different review sites quote Vultr's upper price as $540, $640 and $1,000 per month, which is a good sign that none of them is tracking the current price list. Treat the table as a shape, not a quote, and confirm the figure on the order screen.

## The four differences that actually decide it

### 1. One has a hypervisor, the other doesn't

Bare Metal strips out the virtualization layer entirely. Vultr's own wording is that the hardware is "100% all yours," with no metered CPU or IOPS limits and no shared resources, which matters for workloads that behave badly under a hypervisor. Dedicated Cloud still runs on Vultr's platform, so you keep fast provisioning and the option to upload your own ISO, but the CPU, RAM and disk you rent are reserved rather than shared.

### 2. 10GbE versus 1GbE changes the bandwidth math

Every Bare Metal instance includes a burstable 10GbE connection, but the plan listing pairs it with just 5TB of monthly transfer. Dedicated Cloud gives you a 1GbE uplink with up to 40,000GB of traffic. A fast pipe with a small allowance and a slower pipe with a huge allowance are built for different jobs: short bursts of heavy compute versus steady outbound traffic.

### 3. Neither line runs everywhere

Bare Metal covers 7 of Vultr's 15 regions. Dedicated Cloud covers 4. If your users are in Sydney, São Paulo or Seoul, neither dedicated product is available there, and no amount of price comparison fixes that.

### 4. A whole server versus a quarter of one

Dedicated Cloud's 25% rental is unusual and genuinely useful when you want reserved resources but can't justify a full machine. Bare Metal has no fractional option. You either take the whole box or you don't.

One extra detail for anyone expecting attack traffic: all North American Dedicated Cloud instances include 10Gbps DDoS protection at no cost. Protection against attacks above 10Gbps was described as coming soon for a nominal hourly fee, so don't assume unlimited mitigation.

## Three places money leaks out

**Hourly billing is not pay-as-you-go in the way people assume.** An instance in a stopped state still reserves RAM, SSD, IP addresses and CPU cores, and keeps billing until it is fully destroyed. Shutting a server down for a week to save money doesn't work. You have to destroy it.

**There are no refunds.** Cancel a service before your prepaid period ends and the remaining balance is not returned, and account credit isn't refunded either. Closing an account also requires destroying every active instance and opening a support ticket first.

**Trying it for an hour costs an hour, not a click.** Because of the two rules above, the sensible way to test a plan is to deploy it, run your benchmark, and destroy it the same day.

👉 [Compare that with SpinServers' instant-provisioning Dallas and San Jose servers](https://bit.ly/Spinservers)

## Support and what the reviews say

Vultr's support runs on email and phone. There is no live chat, and ticket hours are listed as weekday 9:00 to 18:00 EDT. For a platform aimed at developers who deploy through an API, that's a gap worth knowing about before something breaks at 2am.

Third-party scores are not flattering: Hostadvice shows 2.2 and Trustpilot 1.7 for Vultr. The page carrying those numbers is old, so read them as a rough signal about how polarizing the service can be rather than a current measurement.

Reviewers also note what Vultr doesn't sell: no shared hosting, no managed WordPress, no domain registration. It's infrastructure, not a website package.

## Where Vultr's lineup stops fitting

The Vultr dedicated range is narrow by design. Four Dedicated Cloud sizes, one Bare Metal listing, seven regions for the bare metal product, and bandwidth allowances measured in single-digit terabytes on the physical side.

SpinServers runs dedicated hardware in Dallas, Texas and San Jose, California, and the Dallas list looks like this:

| Configuration | CPU / RAM | Storage | Network | From | Order |
| --- | --- | --- | --- | --- | --- |
| Intel Xeon E3-1280 v5 | 4C/8T @ 3.7GHz turbo / 32GB DDR4 ECC | 1TB M.2 NVMe | 30TB on a 10Gbps port | $79/mo | [View this server](https://bit.ly/Spinservers) |
| Dual Intel Xeon E5-2630L v3 | 16C/32T @ 2.90GHz turbo / 128GB DDR4 ECC | 1TB NVMe | 30TB on a 10Gbps port | $235/mo | [View this server](https://bit.ly/Spinservers) |
| Dual Intel Xeon Gold 6148 | 40C/80T @ 3.70GHz turbo / 256GB DDR4 | 2×1.92TB SSD | 30TB, 2×10Gbps ports (LACP) | $390/mo | [View this server](https://bit.ly/Spinservers) |
| Dual Intel Xeon Platinum 8173M | 56C/112T @ 3.50GHz turbo / 512GB DDR4 | 4×1.92TB SSD | 30TB, 2×10Gbps ports (LACP) | Listed without a starting price | [View this server](https://bit.ly/Spinservers) |

All four include at least one IPv4 address and auto-provision, so the box is ready without a manual setup queue. The San Jose page lists a wider, frequently changing set of configurations, from 4 cores/8 threads with 32GB and 1TB NVMe up to 32 cores/64 threads with 512GB and 2×3.84TB SSD, every one on dual 10Gbps ports with 30TB of transfer.

## The same money, compared directly

Vultr's Bare Metal listing at $120/month buys 8 CPU, 32GB RAM, 480GB of SSD and 5TB of transfer. SpinServers' $79/month Dallas box buys fewer cores (4 cores, 8 threads) but the same 32GB of ECC memory, twice the local NVMe, and **six times the monthly transfer** on a 10Gbps port. Step up to $235 and you get 16 cores/32 threads with 128GB of memory, which is a configuration Vultr's dedicated lines don't reach at any published price.

The counterargument is real: SpinServers only operates in two US locations. If your application needs to sit close to users in Amsterdam, Singapore or Tokyo, Vultr is the only one of the two that can help, and paying $120 for a smaller bandwidth allowance is simply the cost of that geography.

## Who should pick which

**Take Vultr Bare Metal if** you need a non-virtualized environment in Europe or Asia, you want to create and destroy servers by API on an hourly cycle, or you need Windows or FreeBSD on physical hardware. The seven regions, including Amsterdam and Singapore, are the reason to accept 5TB of transfer and a higher monthly figure.

**Take Vultr Dedicated Cloud if** reserved vCPUs are enough and you want to rent a quarter or half of a machine rather than all of it. Tokyo availability and the free 10Gbps DDoS protection on North American instances are the two features that don't have an equivalent here.

**Take SpinServers if** your users are in North America, your workload wants memory, NVMe and outbound bandwidth more than it wants a second continent, and you'd rather pay $79 than $120 to start. Instant provisioning means you can test the actual hardware the same afternoon.

**Look elsewhere entirely if** you want shared hosting, a managed WordPress install, or to buy a domain in the same cart. Neither provider does any of that.

## Before you place an order

Confirm the region first, because a plan you can't deploy in your target city is a plan you can't use. Then confirm two billing rules: whether stopping the instance stops the charge (on Vultr it does not, only destroying does), and what happens to prepaid credit if you cancel early (on Vultr it is not refunded). Both rules are easy to discover after the fact and annoying to discover at the end of a month.

👉 [Check current SpinServers availability and pricing in Dallas and San Jose](https://bit.ly/Spinservers)
