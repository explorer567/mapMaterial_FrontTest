```
# 检查是否配置了代理
git config --global http.proxy
git config --global https.proxy
git config http.proxy      # 检查当前仓库局部设置（非全局）
git config https.proxy

# 设置环境变量
set HTTP_PROXY=http://127.0.0.1:7890
set HTTPS_PROXY=http://127.0.0.1:7890

# 或者为Git配置
git config --global http.proxy http://127.0.0.1:7890
git config --global https.proxy http://127.0.0.1:7890

# 拉取后需取消，配置。才能正确访问国内的其他网址。
  不然拉取其他国内网址也会默认走代理。
# 取消git代理设置
git config --global --unset http.proxy
git config --global --unset https.proxy

# 或者临时取消环境变量
set HTTP_PROXY=
set HTTPS_PROXY=
```
```
# 项目级配置
git config http.proxy http://127.0.0.1:7890
git config https.proxy http://127.0.0.1:7890
# 移除
git config --local --unset http.proxy
git config --local --unset https.proxy
或
git config --unset http.proxy
git config --unset https.proxy
```
```
验证：
# 查看系统级配置【所有用户】
git config --system --list

# 查看全局（用户级）配置【当前用户】
git config --global --list

# 查看项目级配置（需要在项目目录内）
git config --local --list

# 查看最终生效的配置（会合并所有级别）
git config --list

```

