# Update Conference Krakow 2026 - Beyond Trust: Building Community-Driven Security Analysis for Your .NET Software Supply Chain

In today's development, approximately 80% of our software deployments consist of code written by someone else. Using existing libraries and packages is essential for productivity and avoiding reinventing the wheel, this dependency on third-party code introduces security risks that can be hard to address in a good way.

First part of this talk will focus on the challenges of securing our software supply chain, particularly on NuGet package security and the hidden threats lurking within all of our used dependencies. We'll examine how traditional approaches fall short when it comes to identifying planted malware, risky APIs, and other security vulnerabilities embedded deep within the packages we trust.

While tools like the OpenSSF Security Scorecard provide valuable metrics, they only scratch the surface of what's needed for comprehensive supply chain security. What if we could go deeper? What if we had detailed analysis of NuGet package contents, automated detection of risky API usage?

Join me as I introduce Fennec Labs, a community-focused OSS project designed to help out with how we analyze and secure our software dependencies. I'll demonstrate how this tool enables developers to collaboratively identify security risks, share insights, and make more informed decisions about the NuGet packages they integrate into their applications.

Whether you're a security-conscious developer, a DevOps engineer, or someone responsible for maintaining your organization's software supply chain, this session will provide practical insights and tools to help you level up your security game and protect your applications from supply chain attacks.

## Fennec Labs CLI

Fennec Labs has not been released to NuGet at this point. You can either add the following `nuget.config` on your system and get the tool installed on your system. 

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
 <packageSources>
    <add key="fennec-feedz" value="https://f.feedz.io/fennec/labs/nuget/index.json" /> 
</packageSources>
</configuration>
```

And then run the following command to get it installed:

```bash
dotnet tool install --global fennec.labs --version 0.7.5-preview.1
```

Or clone this repo and execute the command shown below to get it installed as global tool on your system.

```bash
dotnet tool install --global --add-source ./FennecLabs Fennec.Labs --version 0.7.5-preview.2
```
## Demo video's

- Scorecards : https://youtu.be/l5E0civv82U?t=1584
- Reproduciblity: https://youtu.be/l5E0civv82U?t=2048
- Instrument: https://youtu.be/l5E0civv82U?t=2219
- Compare: https://youtu.be/l5E0civv82U?t=2487
