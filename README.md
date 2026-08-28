# MCPBench-Dev


----
#### NOTE: this readme is still under construction, please do not hesitiate to ping me (junlong) at any time. You are always welcomed!
----
### Before Start

#### Use a Saperate Branch
Please set a saperate branch for yourselves in for development. Do not push to master directly without notification, thanks!

#### About Proxy
Please see `FAQs/setup_proxy.md` to see how to set up a proxy for your terminal/cmd. I only provide some general guides, so you may need to see more effort to solve the proxy issue, e.g. via Google Search and asking LLMs.

You may need to configure some proxies for your MCP servers, e.g. `configs/mcp_servers/playwright.yaml`. You just need to uncomment the corresponding lines, the code will automatically load proxy from `configs/global_configs.py`.

However, it's hard for us to totally understand your own network environment, so you still need to try yourself for this issue. In our case, all servers are runnable on a Linux machine with proper and robust network connection.

### Preparation

#### LLM APIs
You should have a `configs/global_configs.py`, with the template in `configs/global_configs_example.py`

#### Basic Env Setup
0. install uv

    please refer to the official [website](https://github.com/astral-sh/uv), you may need to switch on some proxies in this process

    you should be able to see some guide after `uv`

1. install this project
    ```
    git clone https://github.com/hkust-nlp/mcpbench_dev.git
    uv init mcpbench_dev --python=3.12
    cd mcpbench_dev
    ```

2. set up pypi mirror (optional)
    for chinese users who do not want to switch on proxy, you can add the following lines to `pyproject.toml`

    ```
    [[tool.uv.index]]
    url = "https://mirrors.tuna.tsinghua.edu.cn/pypi/web/simple"
    default = true
    ```

    to use Tsinghua Pypi mirror

3. install npm (see `FAQs/npm_install.md`)
