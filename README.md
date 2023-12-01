<p align="center"><img src="https://avatars.githubusercontent.com/u/91626055?v=4" width="128" /></p>

<div align="center">

# Aiko-Server

Aiko-Server Projects

[![](https://img.shields.io/badge/Telegram-group-green?style=flat-square)](https://t.me/aikoaikoaikoaiko)
[![](https://img.shields.io/badge/Telegram-blue?style=flat-square)](https://t.me/Tele_Aiko)
[![](https://img.shields.io/github/downloads/AikoPanel/Aiko-Server/total.svg?style=flat-square)](https://github.com/AikoPanel/Aiko-Server/releases)
[![](https://img.shields.io/github/v/release/AikoPanel/Aiko-Server?style=flat-square)](https://github.com/AikoPanel/Aiko-Server/releases)
[![docker](https://img.shields.io/docker/v/aikocute/aikocutehotme?label=Docker%20image&sort=semver)](https://hub.docker.com/r/aikocute/aikocutehotme)
[![Go-Report](https://goreportcard.com/badge/github.com/AikoPanel/Aiko-Server?style=flat-square)](https://goreportcard.com/report/github.com/AikoPanel/Aiko-Server)

</div>

# Description of Aiko-Server

Aiko-Server Supports Various Panels (AikoPanel, V2AikoPanel, etc.)

An Xray-based back-end framework, supporting V2ay, Trojan, Shadowsocks protocols, extremely easily extensible and supporting multi-panel connection。

If you like this project, you can click the star + view in the upper right corner to track the progress of this project.

## Disclaimer

This project is for my personal learning, development and maintenance only, I do not guarantee the availability and I am not responsible for any consequences resulting from using this software.

## Featured

- Open source `This version depends on the happy mood`
- Supports multiple protocols V2ray, Trojan, Shadowsocks.
- Supports new features like Vless and XTLS.
- Supports single connection to multiple boards and nodes without rebooting.
- Online IP support is limited
- Support node port level, user level rate limit.
- Simple and clear configuration.
- Modify the configuration to automatically restart the instance.
- Easy to compile and upgrade, can quickly update core version, support new Xray-core features.
- Support UDP and many other functions

## Featured

| Featured                                   | VMess | Trojan | Shadowsocks | VLESS |
| ------------------------------------------ | ----- | ------ | ----------- | ----- |
| Get button info                            | √     | √      | √           | √     |
| Get user information                       | √     | √      | √           | √     |
| User traffic statistics                    | √     | √      | √           | √     |
| Report server information                  | √     | √      | √           | √     |
| Automatic registration of TLS certificates | √     | √      | √           | √     |
| auto-renew tls certificate                 | √     | √      | √           | √     |
| Number of people online                    | √     | √      | √           | √     |
| Online User Restrictions                   | √     | √      | √           | √     |
| Audit rules                                | √     | √      | √           | √     |
| Node port speed limit                      | √     | √      | √           | √     |
| User speed limit                           | √     | √      | √           | √     |
| Custom DNS                                 | √     | √      | √           | √     |

## User interface support

| Panel                                                  | VMess | Trojan | Shadowsocks | VLESS  |
| ------------------------------------------------------ | ----- | ------ | ----------- | ------ |
| AikoPanel                                              | √     | √      | √           | √      |
| V2AikoPanel                                            | √     | √      | √           | √      |


## Command support

- [x] `aiko-server` - Aiko-Server command
- [x] `aiko-server x25519` - X25519 certificate management (Vless-Reality)
- [x] `aiko-server cert` - Create TLS certificate management

**Note: The command is not supported in the docker version and if you have Command New for it pls commit it**

## Software installation - release

```
wget --no-check-certificate -O Aiko-Server.sh https://raw.githubusercontent.com/AikoPanelv1/Aiko-Server-Script/master/install.sh && bash Aiko-Server.sh
```

## Aiko-Server Community Support

[Telegram](https://t.me/AikoServer_Community)

**Note: Because I'm lazy to write documents, if anyone volunteers to write documents for aiko-server, please contact me (use English).**

### Config File 
```yaml
Nodes:
  - PanelType: "AikoPanelv2" # Panel type: AikoPanel, AikoPanelv2
    ApiConfig:
      ApiHost: "http://127.0.0.1:667"
      ApiKey: "123"
      NodeID: 41
      NodeType: V2ray # Node type: V2ray, Shadowsocks, Trojan
      Timeout: 30 # Timeout for the api request
      EnableVless: false # Enable Vless for V2ray Type
      RuleListPath: # /etc/Aiko-Server/rulelist Path to local rulelist file
    ControllerConfig:
      EnableProxyProtocol: false
      DisableLocalREALITYConfig: false
      EnableREALITY: false
      REALITYConfigs:
        Show: true
      CertConfig:
        CertMode: none # Option about how to get certificate: none, file
        CertFile: /etc/Aiko-Server/cert/aiko_server.cert # Provided if the CertMode is file
        KeyFile: /etc/Aiko-Server/cert/aiko_server.key
```

## Stargazers over time

[![Stargazers over time](https://starchart.cc/AikoPanel/Aiko-Server.svg)](https://starchart.cc/AikoPanel/Aiko-Server)
