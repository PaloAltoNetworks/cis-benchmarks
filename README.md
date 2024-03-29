# Important Please Read
The CIS Benchmark Skillet is no longer being actively supported or maintained. Users can submit merge requests to the repository for features they would like to add or to update the skillet but beyond that the team is not actively working on this anymore.


# CIS Benchmark Report

The [Center for Internet Security (CIS)](https://www.cisecurity.org)
 provides a benchmark checklist
 to assess if a Palo Alto Networks NGFW meets their recommended security
  requirements.

The [currently released benchmark](https://www.cisecurity.org/benchmark/palo_alto_networks/)
 is for PAN-OS 9.x (CIS Palo Alto Firewall 9 Benchmark version 1.0.0)

Instead of manually working through the checklist, 
this solution allows a user to query PAN-OS NGFW configuration and system
information to determine alignment with the CIS benchmarks.

## Prerequisites

To get the full benefit of this assessment, API access to the NGFW is
required. This allows the solution to query active system information
such as license states and the currently installed list of PAN-DB URL
categories.

API access can be direct to the NGFW or accessed through Panorama using the
NGFW serial number.

## Quick Start Options

### panhandler

> panhandler 4.x or later is required to run this assessment and generate the 
output report

* import this repository into panhandler
* run the workflow skillet 'Run CIS benchmark assessment'
* review the output report

## Viewing the Assessment Report

The embedded report provides the following information

* summary of test results by type
* all benchmarks listed with Level and if scored per the CIS documentation
* document link for each benchmark providing audit and remediation details
* hovering over the result provides pop-up contextual information to assist
 with manual remediation where required

> the result type 'action required' is used where manual investigation is
> required to determine benchmark results. Use the benchmark audit
> information contained in the documentation link

## Known Limitations and Issues

* Some of the benchmarks are not currently implemented either due to a
 requirement that is not specific to the NGFW implementation or requires
  select user input that may come in a future release. These are flagged with
   'Action Required' and users should review the manual audit and remediation
    steps for these benchmarks  
* The current solution can pull NGFW information through a Panorama interface
 but does not currently support query of a Panorama configuration
* The current solution does not provide automated remediation requiring users
 to review the manual remediation steps found in the benchmark documentation
* The current solution is specific to PAN-OS 9.x. It can be used with a 10.x
 NGFW without guarantee that all results will be accurate due to feature
  support and config file format changes between releases


## Support Policy
The code and templates in the repo are released under an as-is, best effort,
support policy. These scripts should be seen as community supported and
Palo Alto Networks will contribute our expertise as and when possible.
We do not provide technical support or help in using or troubleshooting the
components of the project through our normal support options such as
Palo Alto Networks support teams, or ASC (Authorized Support Centers)
partners and backline support options. The underlying product used
(the VM-Series firewall) by the scripts or templates are still supported,
but the support is only for the product functionality and not for help in
deploying or using the template or script itself. Unless explicitly tagged,
all projects or work posted in our GitHub repository
(at https://github.com/PaloAltoNetworks) or sites other than our official
Downloads page on https://support.paloaltonetworks.com are provided under
the best effort policy.
