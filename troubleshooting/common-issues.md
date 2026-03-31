# Azure Troubleshooting Notes

## Overview
This document captures key issues encountered during Azure lab setup and the troubleshooting steps used to resolve them.

---

## Issue 1: Region Mismatch

### Problem
Virtual network was not visible when creating a virtual machine.

### Root Cause
Resources were deployed in different Azure regions, causing incompatibility between network and compute resources.

### Resolution
Aligned all resources (VNet, VM, and supporting services) within the same region.

---

## Issue 2: VM Size Availability

### Problem
Selected VM size (e.g., B-series) was not available.

### Root Cause
Certain VM sizes are not available in all Azure regions.

### Resolution
Changed region to one supporting the desired VM size or selected an alternative size.

---

## Issue 3: NSG Blocking Access

### Problem
Unable to connect to virtual machine.

### Root Cause
Network Security Group rules were not configured to allow inbound traffic.

### Resolution
Configured inbound NSG rules to allow required ports (e.g., SSH on 22, RDP on 3389).

---

## Lessons Learned

- Cloud resources must be planned with region alignment in mind
- NSG rules directly impact connectivity and must be validated early
- Troubleshooting builds deeper understanding of cloud networking behavior
- Infrastructure dependencies should be considered before deployment