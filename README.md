# OTSec-PS: IEC 62443 Compliance Toolkit

**OTSec-PS** is a PowerShell-based toolkit designed to help implement and audit security controls for **Operational Technology (OT)** systems in compliance with the **IEC 62443** standard. The toolkit provides modular scripts to enhance security for authentication, access control, system integrity, and other critical areas of industrial automation.

## Key Features

- **Modular Design**: Each IEC 62443 foundational requirement (FR) is covered by separate PowerShell modules.
- **Authentication Control (FR1)**: Manage user and process authentication.
- **Access Control (FR2)**: Enforce role-based and policy-based access control.
- **System Integrity (FR3)**: Verify the integrity of communications and software.
- **Automated Compliance Testing**: Simplify the process of auditing OT system security.

## Getting Started

### Prerequisites

- **PowerShell** 5.1+ (Windows) or **PowerShell Core** (cross-platform).
- Administrative access to systems for performing security-related tasks.

### Installation

1. Clone the repository to your local machine:
    ```bash
    git clone https://github.com/yourusername/OTSec-PS.git
    ```

2. Navigate to the repository:
    ```bash
    cd OTSec-PS
    ```

## Usage

### Example: Authentication Control (FR1)

To enforce authentication control and run tests:

```powershell
# Enforce password-based authentication
.\modules\FR1-Authentication\Invoke-AuthControl.ps1 -UserName "Admin" -AuthenticationMethod "Password"

# Test authentication at Security Level 1
.\modules\FR1-Authentication\Test-Authentication.ps1 -UserName "Admin" -AuthLevel "SL1"
