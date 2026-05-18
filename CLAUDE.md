# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with this repository.

## Project Overview

This is a proxy routing rule set repository (`science-rule`). It provides three categories of domain/IP rules consumed by Clash-like proxy clients via HTTP providers (jsdelivr CDN or GitHub raw).

## Directory Structure

```
ruleset/
  direct.yaml   — DIRECT 直连规则：直连域名和 IP（内网段、可信服务）
  proxy.yaml    — PROXY 代理规则：需走代理的服务（ChatGPT、Claude 等 AI 站点）
  llm.yaml      — LLM 杂项规则：开发工具、游戏、视频等需要代理的域名
```

## YAML 格式约定

每个规则文件使用 `payload` 列表，条目格式遵循 Clash rule provider 规范：

- `DOMAIN-SUFFIX,+.example.com` — 匹配域名及其子域名
- `DOMAIN-SUFFIX,exact.example.com` — 精确域名匹配
- `IP-CIDR,x.x.x.x/xx` — IP 段匹配
- `PROCESS-NAME,AppName` — 进程名匹配

## 工作流

- 添加新规则时，根据用途归入对应 YAML 文件
- 规则变更后提交并 push，CDN 会自动刷新（客户端配置了 `interval: 86400`）
- 无构建、测试、lint 流程，纯配置仓库
