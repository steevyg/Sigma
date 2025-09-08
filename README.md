
## Usage

1.  **Convert Rules:** Use the [Sigma CLI](https://github.com/SigmaHQ/sigma-cli) to convert these `.yml` rules for your specific SIEM (e.g., Splunk, Elasticsearch, Azure Sentinel).
    sigma convert -t splunk rules/windows/wmi/wmi_event_subscription_remote_execution.yml
2.  **Deploy:** Import the converted query into your SIEM.
3.  **Tune:** Adjust parameters (e.g., `falsepositives`, exclusions) to fit your environment's baseline before deploying to production.

## Requirements

*   A SIEM that supports Sigma (e.g., Splunk, Elastic Stack, Microsoft Sentinel).
*   **Recommended:** Sysmon configured with a comprehensive logging policy (e.g., SwiftOnSecurity or Olaf Hartong's config).
*   Windows Event Logging enabled for specific services (WMI-Activity, PowerShell, Command Auditing).

## Contributing

Contributions and suggestions are welcome! Please feel free to open an Issue or submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer

These rules are provided as a starting point for detection engineering. Always test and tune them extensively in your own lab environment before deploying to production. 
