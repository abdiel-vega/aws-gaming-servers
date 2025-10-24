# AWS Gaming Server Infrastructure

Secure, scalable gaming server infrastructure on AWS with cloud architecture and security best practices.

## Technologies

**AWS Services:** VPC, EC2, CloudWatch, IAM, S3  
**OS/Tools:** Ubuntu 22.04, systemd, Bash  
**Security:** Security Groups, NACLs, MFA, SSH key pairs

## Architecture

- **VPC:** Isolated network with public/private subnet segmentation
- **Compute:** t3.medium EC2 instances with scheduled start/stop
- **Security:** Least-privilege security groups, restricted SSH access
- **Monitoring:** CloudWatch metrics and custom alarms
- **Backup:** Automated daily snapshots to S3

[View Architecture Diagrams →](docs/architecture/diagrams/)

## Key Features

### Security
- MFA-enabled root account with restricted access
- SSH access limited to specific IP ranges
- Application-level authentication (whitelist + passwords)
- CloudWatch logging for all system events
- Automated security group auditing

### Cost Optimization
- Instance scheduling (auto-stop during off-hours)
- Right-sized instances based on player load
- Lifecycle policies for snapshot retention

### Reliability
- Automated backups every 6 hours
- Health checks with CloudWatch alarms
- Documented recovery procedures
- 99.5%+ uptime over 6 months

## Documentation

- [Architecture Overview](docs/architecture/architecture-overview.md)
- [Security Hardening](docs/security/hardening-guide.md)
- [Troubleshooting Guide](docs/operations/troubleshooting.md)
- [Cost Analysis](docs/cost-analysis.md)
- [Architecture Decisions](docs/adr/)

## Lessons Learned

**VPC Design:** Initially used default VPC; redesigned with dedicated VPC for better isolation and control.

**Security Groups:** Learned importance of granular rules over broad access; implemented least-privilege principle.

**Cost Management:** Discovered instance scheduling reduced costs by 60% during non-peak hours.

**Monitoring:** CloudWatch custom metrics provided insights that basic monitoring missed.

## Contact

[Abdiel Y Vega Velez] - [https://www.linkedin.com/in/abdiel-vega2004/] 
[abdiel.vega@outlook.com]
+1 (787) 949 5751