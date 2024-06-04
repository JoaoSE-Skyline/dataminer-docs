---
uid: General_Main_Release_10.3.0_CU17
---

# General Main Release 10.3.0 CU17 – Preview

> [!IMPORTANT]
> We are still working on this release. Some release notes may still be modified or moved to a later release. Check back soon for updates!

> [!TIP]
> For information on how to upgrade DataMiner, see [Upgrading a DataMiner Agent](xref:Upgrading_a_DataMiner_Agent).

### Enhancements

#### 'Security Advisory' BPA test will no longer report an issue when NATS does not have TLS enabled on a single DMA [ID_39792]

<!-- MR 10.3.0 [CU17]/10.4.0 [CU5] - FR 10.4.8 -->

When the [Security Advisory](xref:BPA_Security_Advisory) BPA test was run on a single DataMiner Agent of which firewall port 4222 and 6222 were closed, up to now, it would report an issue saying that NATS did not have TLS enabled.

As NATS does not need TLS enabled on single DataMiner Agents, from now on, the [Security Advisory](xref:BPA_Security_Advisory) BPA test will only report an issue regarding NATS TLS when, on a single DataMiner Agent, firewall ports 4222 and 6222 are open.

#### 'Security Advisory' BPA test: Enhanced testing of HTTP and HTTPS connections [ID_39813]

<!-- MR 10.3.0 [CU17]/10.4.0 [CU5] - FR 10.4.8 -->

A number of enhancements have been made to the [Security Advisory](xref:BPA_Security_Advisory) BPA test with regard to the testing of HTTP and HTTPS connections.

### Fixes

#### SLLogCollector: 'Access is denied' errors [ID_39364]

<!-- MR 10.3.0 [CU17]/10.4.0 [CU5] - FR 10.4.8 -->

In some cases, SLLogCollector would not have the required permissions to access process objects or execute certain WMI queries. As a result, `Access is denied` errors would be added to the *SLLogCollector.txt* log file.

#### Table row discrepancy between SLElement and SLProtocol [ID_39645]

<!-- MR 10.3.0 [CU17]/10.4.0 [CU5] - FR 10.4.8 -->

Due to a locking issue, in some cases, SLProtocol and SLElement could end up with different sets of table rows stored in memory.

#### Service & Resource Management: Booking events would be executed in incorrect order [ID_39748]

<!-- MR 10.3.0 [CU17]/10.4.0 [CU5] - FR 10.4.8 -->

In some cases, SLNet would execute booking events in incorrect order.

#### Problem with SLASPConnection when an email message could not be delivered [ID_39759]

<!-- MR 10.3.0 [CU17]/10.4.0 [CU5] - FR 10.4.8 -->

In some cases, a fatal error could occur in SLASPConnection when an email message could not be delivered.