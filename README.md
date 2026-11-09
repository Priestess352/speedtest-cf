# 🚀 Speedtest-CF

基于 Cloudflare Workers 的测速服务，提供稳定可靠的网络测速功能。

## ✨ 功能特点

- 基于 Cloudflare Workers 部署，全球节点覆盖
- 支持自定义测速文件大小
- 可绑定自定义域名，避免被节点屏蔽
- 简单易用的配置方式
- 无需服务器维护

## 🎯 使用场景

- 网络服务提供商测速
- 个人网络质量测试
- 服务器网络性能评估
- 网络优化参考

## 📦 部署步骤

1. 登录 [Cloudflare Workers](https://workers.cloudflare.com/)
2. 创建新的 Worker
3. 将 `worker.js` 代码复制到编辑器中
4. 点击 "Save and Deploy" 部署
5. 绑定自定义域名（可选但推荐）

## ⚙️ 配置说明

### 测速地址配置

```yaml
# 使用字节单位
# 100MB 测速文件
speed-test-url: https://your-domain/speedtest?bytes=104857600

# 1GB 测速文件
speed-test-url: https://your-domain/speedtest?bytes=1073741824

# 使用M单位（更易读）
# 100MB 测速文件
speed-test-url: https://your-domain/speedtest?bytes=100M

# 1GB 测速文件
speed-test-url: https://your-domain/speedtest?bytes=1024M
```

### 参数说明

- `bytes`: 测速文件大小
  - 支持字节单位：100MB = 104857600 字节
  - 支持M单位：100M = 100MB，1024M = 1GB
  - 两种单位可以互换使用

## ⚠️ 注意事项

1. 建议使用自定义域名，避免被节点屏蔽
2. 测速文件大小应根据实际需求选择
3. 避免频繁进行大文件测速
4. 注意遵守 Cloudflare Workers 的使用限制

## ❓ 常见问题

### Q: 为什么需要自定义域名？
A: 使用自定义域名可以避免被某些网络节点屏蔽，提高测速成功率。

### Q: 如何选择合适的测速文件大小？
A: 建议根据实际网络环境选择：
- 低速网络：使用 100MB 文件
- 高速网络：使用 1GB 文件

### Q: 测速结果不准确怎么办？
A: 请检查：
1. 网络连接是否稳定
2. 是否使用了自定义域名
3. 测速文件大小是否合适

## 📝 更新日志

- 2024-03-xx: 初始版本发布
