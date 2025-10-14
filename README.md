# science rule

## 类别：
- direct classical
- llm domain
- proxy domain
## 使用

最新
```yaml
rule-providers:
  shaw-direct:
    type: http
    behavior: classical
    url: "https://cdn.jsdelivr.net/gh/x13945/science-rule@v1.0.1/ruleset/direct.yaml"
    path: ./ruleset/shaw-direct.yaml
    interval: 86400
  shaw-proxy:
    type: http
    behavior: domain
    url: "https://cdn.jsdelivr.net/gh/x13945/science-rule@v1.0.1/ruleset/proxy.yaml"
    path: ./ruleset/shaw-proxy.yaml
    interval: 86400
  shaw-llm:
    type: http
    behavior: classical
    url: "https://cdn.jsdelivr.net/gh/x13945/science-rule@v1.0.1/ruleset/llm.yaml"
    path: ./ruleset/shaw-llm.yaml
    interval: 86400
```

**jsdeliver**
```
https://cdn.jsdelivr.net/gh/x13945/science-rule/ruleset/direct.yaml
https://cdn.jsdelivr.net/gh/x13945/science-rule/ruleset/llm.yaml
https://cdn.jsdelivr.net/gh/x13945/science-rule/ruleset/proxy.yaml

```
**github**
```
https://raw.githubusercontent.com/x13945/science-rule/master/ruleset/direct.yaml
https://raw.githubusercontent.com/x13945/science-rule/master/ruleset/llm.yaml
https://raw.githubusercontent.com/x13945/science-rule/master/ruleset/proxy.yaml
```
