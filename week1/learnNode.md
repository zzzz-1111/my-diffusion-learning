# week1学习笔记

## github基本使用
```bash
# 2. 查看状态（哪些文件被修改了）
git status

# 3. 添加文件到暂存区
git add note1.md           # 添加单个文件
git add .                  # 添加所有修改的文件

# 4. 提交到本地仓库
git commit -m "添加第一个学习笔记"

# 5. 推送到 GitHub
git push origin main
```

### **同步远程：**

```bash
Copygit pull origin main     # 拉取远程更新（多设备同步时用）
git push origin main     # 推送本地更新到远程
```

## diffusion概念 -- tutorial-4

SDE: stochastic differential equations

OU: Ornstein-Uhlenbeck process

$$dX_t=-\mu X_tdt+\sigma dB_t$$

$\mu, \sigma$是常数，在教程中设置成了$\mu=1/2, \sigma = 1$

SGM: Score-based generative modelling

- 任何OU过程最后总是会变成高斯分布
- 我们可以进行OU的逆过程

OU的正向过程：
$$dX_t=f(t, X_t)dt+G(t)dB_t$$
逆向过程
$$dX_t=f(t, X_t)-G(t)^2\nabla_x\log p_t$$

OU的解
$$dX_t = -\mu X_t dt + \sigma dB_t$$