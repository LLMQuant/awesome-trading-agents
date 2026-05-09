<!--lint disable awesome-heading double-link-->

<div align="center">

<img src="assets/header-generated-v2.png" alt="Awesome Trading Agents — The Trading Agentic Stack" width="760" />

<p><strong>English</strong> · <a href="README.zh-CN.md">简体中文</a></p>

<p>
  <a href="https://awesome.re"><img src="https://awesome.re/badge.svg" alt="Awesome" /></a>
  <a href="https://github.com/LLMQuant/awesome-trading-agents/stargazers"><img src="https://img.shields.io/github/stars/LLMQuant/awesome-trading-agents?style=flat" alt="GitHub stars" /></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg" alt="License: CC0-1.0" /></a>
  <a href="https://github.com/topics/trading-agents"><img src="https://img.shields.io/badge/topics-trading--agents%20%C2%B7%20mcp--servers%20%C2%B7%20agent--skills-blue" alt="Topics" /></a>
  <a href="https://github.com/LLMQuant/awesome-trading-agents/commits"><img src="https://img.shields.io/github/last-commit/LLMQuant/awesome-trading-agents" alt="Last commit" /></a>
  <a href="README.zh-CN.md"><img src="https://img.shields.io/badge/bilingual-zh%20%C2%B7%20en-708090" alt="Bilingual" /></a>
</p>

</div>

Awesome Trading Agents collects open-source projects where LLMs help research markets, make trading decisions, or connect agents to market data and execution tools. The list focuses on three building blocks: Agents, MCPs, and Skills. It does not try to cover classic quant libraries, time-series models, or reinforcement-learning trading bots; those are better served by [`georgezouq/awesome-ai-in-finance`](https://github.com/georgezouq/awesome-ai-in-finance) and [`wilsonfreitas/awesome-quant`](https://github.com/wilsonfreitas/awesome-quant). Entries are selected for public code or artifacts, clear LLM-driven behavior, recent activity, useful documentation, a distinct role, and visible adoption. Stewarded by the [LLMQuant](https://llmquant.com) community.

> [!TIP]
> **If you only read three:**
>
> - **Agents** — [TauricResearch/TradingAgents](#agents-tradingagents) · [virattt/ai-hedge-fund](#agents-ai-hedge-fund) · [HKUDS/AI-Trader](#agents-ai-trader)
> - **MCPs** — [alpacahq/alpaca-mcp-server](#mcps-alpaca) · [krakenfx/kraken-cli](#mcps-kraken-cli) · [financial-datasets/mcp-server](#mcps-financial-datasets)
> - **Skills** — [tradermonty/claude-trading-skills](#skills-claude-trading-skills) · [himself65/finance-skills](#skills-finance-skills) · [RKiding/Awesome-finance-skills](#skills-alphaear)

> [!NOTE]
> Dates are not shown after every item. We still check recent activity before adding or updating a project; the README only keeps details that help readers choose a project, such as official status, forks, or useful pairings.

<!--lint disable awesome-toc-->
## Contents

- [**Agents**](#agents)
  - [Multi-agent trading systems](#agents-multi-agent)
  - [Single-agent end-to-end traders](#agents-single-agent)
  - [Research / equity-research copilots](#agents-research-copilots)
  - [Real-money / competition experiments](#agents-real-money)
  - [Prediction-market specialists](#agents-prediction-market)
  - [Benchmarks & evaluations](#agents-benchmarks)
  - [Strategy coding / self-improving agents](#agents-strategy-coding)
- [**MCPs**](#mcps)
  - [Market data / data providers](#mcps-market-data)
  - [Brokerage / exchange trading](#mcps-brokerage)
  - [Research tools / analysis](#mcps-research-tools)
  - [TradingView bridge](#mcps-tradingview)
  - [Prediction markets](#mcps-prediction-market)
  - [Strategy / backtesting platforms](#mcps-backtesting)
- [**Skills**](#skills)
  - [Equity research](#skills-equity-research)
  - [Crypto / DeFi / on-chain](#skills-crypto)
  - [Strategy coding & backtesting](#skills-strategy-coding)
  - [Brokerage execution & portfolio](#skills-brokerage)
- [**Resources**](#resources)
  - [Papers](#resources-papers)
  - [Learn](#resources-learn)
- [Related awesome lists](#related-awesome-lists)

<!--lint enable awesome-toc-->

<a id="agents"></a>
## Agents

<p align="center">
  <img src="assets/section-agents.png" alt="Agents section header" width="760" />
</p>

Agents are projects where an LLM is part of the actual research or trading decision. This includes analyst teams, single-agent traders, research copilots, live trading experiments, benchmarks, and tools that write or improve strategies. The TradingAgents forks are listed at the same level as the original project so the section stays easy to scan.

<a id="agents-multi-agent"></a>
### Multi-agent trading systems

<a id="agents-tradingagents"></a>
- [TauricResearch/TradingAgents](https://github.com/TauricResearch/TradingAgents) - Multi-agent trading framework where analysts, bull/bear researchers, a trader, risk control, and a portfolio manager debate before making a decision; built with LangGraph.
- [hsliuping/TradingAgents-CN](https://github.com/hsliuping/TradingAgents-CN) - Chinese-localised TradingAgents fork tuned for A-shares; Tushare / AkShare data sources + Chinese-language reports + A-share regulatory context. *(← fork of TauricResearch/TradingAgents.)*
- [KylinMountain/TradingAgents-AShare](https://github.com/KylinMountain/TradingAgents-AShare) - A-share rewrite; 15 agents + visual UI + OpenClaw / Claude Code integration + one-click Docker deploy. *(← fork of TauricResearch/TradingAgents.)*
- [oficcejo/aiagents-stock](https://github.com/oficcejo/aiagents-stock) - A-share multi-agent analyst team with dragon-and-tiger list tracking, sector-rotation alerts, and a miniqmt execution hook. *(← inspired by TradingAgents.)*
<a id="agents-ai-trader"></a>
- [HKUDS/AI-Trader](https://github.com/HKUDS/AI-Trader) - "Agent-native trading platform"; any AI agent (OpenClaw / nanobot / Claude Code / Codex / Cursor) registers via SKILL.md and trades live on AI4trade.ai; multi-asset + copy-trading + cross-platform sync.
- [ValueCell-ai/valuecell](https://github.com/ValueCell-ai/valuecell) - Community finance workspace with research, strategy, and news agents; connects to Binance, OKX, and Hyperliquid; includes macOS and Windows desktop apps.
- [AI4Finance-Foundation/FinRobot](https://github.com/AI4Finance-Foundation/FinRobot) - AI4Finance Foundation's open-source finance AI agent platform; useful for academic-style stock research, market forecasting, and report generation.
<a id="agents-vibe-trading"></a>
- [HKUDS/Vibe-Trading](https://github.com/HKUDS/Vibe-Trading) - Personal multi-agent finance workspace from HKUDS Lab; bundles Skills, MCP tools, and swarm presets across A-shares, HK, US, crypto, futures, and forex.
- [brokermr810/QuantDinger](https://github.com/brokermr810/QuantDinger) - Open-source AI quant-trading platform; combines multi-agent research, backtesting, live trading, and multi-exchange routing.
- [The-Swarm-Corporation/AutoHedge](https://github.com/The-Swarm-Corporation/AutoHedge) - "Spin up an autonomous hedge fund in minutes"; applies the Swarms framework to market analysis, risk, and execution; CLI / SDK first.
<a id="agents-langalpha"></a>
- [ginlix-ai/LangAlpha](https://github.com/ginlix-ai/LangAlpha) - "Claude Code for finance"; LangChain + LangGraph multi-agent investment workbench; integrates Agents · MCPs · Skills in one repo.
- [ygwyg/MAHORAGA](https://github.com/ygwyg/MAHORAGA) - TypeScript crypto-trading agent focused on social sentiment analysis and adaptive learning; useful if you want a TypeScript implementation.
- [FinStep-AI/ContestTrade](https://github.com/FinStep-AI/ContestTrade) - Multi-agent trading system where agents compete internally before one view is selected for the final decision.
- [51bitquant/ai-hedge-fund-crypto](https://github.com/51bitquant/ai-hedge-fund-crypto) - Crypto-focused fork of virattt/ai-hedge-fund; multi-timeframe analysis + strategy ensemble + crypto market-data access.
<a id="agents-prism-insight"></a>
- [dragon1086/prism-insight](https://github.com/dragon1086/prism-insight) - Korean-market-focused multi-agent stock-analysis and trading system; built-in MCP integration.
- [Tomortec/CryptoTradingAgents](https://github.com/Tomortec/CryptoTradingAgents) - Multi-agent LLM crypto-trading framework; applies the TradingAgents idea to crypto trading.
- [EthanAlgoX/LLM-TradeBot](https://github.com/EthanAlgoX/LLM-TradeBot) - Multi-agent crypto-trading system; Binance real-time execution + adaptive strategy switching; combines ideas from TradingAgents and nof1.ai.
- [huygiatrng/AlpacaTradingAgent](https://github.com/huygiatrng/AlpacaTradingAgent) - TradingAgents-style multi-agent framework connected to Alpaca for US-equity trading. *(→ pairs with: [alpacahq/alpaca-mcp-server](#mcps-alpaca).)*
- [Yaolinwang/AITD](https://github.com/Yaolinwang/AITD) - "AI Trading Agent for Everyone"; multi-agent project designed for retail users.
- [flash131307/multi-agent-investment](https://github.com/flash131307/multi-agent-investment) - Multi-agent equity-research system that lets LLM agents gather evidence, then uses a separate math layer to produce BUY / NEUTRAL / SELL.
<a id="agents-oracle3"></a>
- [YichengYang-Ethan/oracle3](https://github.com/YichengYang-Ethan/oracle3) - Multi-venue (Kalshi / Polymarket / Solana) prediction-market autonomous agent; Wang-Transform pricing + Kelly criterion + cross-venue arbitrage.
- [Ganador1/FenixAI_tradingBot](https://github.com/Ganador1/FenixAI_tradingBot) - LangGraph + Ollama + CrewAI autonomous trading agent; local-LLM first.
- [ryan-yuuu/crypto-trading-arena](https://github.com/ryan-yuuu/crypto-trading-arena) - Open-source crypto-trading arena; Claude / Claude Code agents compete head-to-head on live crypto data.
- [FareedKhan-dev/multi-agent-trading-system](https://github.com/FareedKhan-dev/multi-agent-trading-system) - "Deep Thinking Trading System" tutorial implementation; beginner-friendly multi-agent example design.
- [Tanglumy/Finance-Bro](https://github.com/Tanglumy/Finance-Bro) - Persona-styled finance "bro" trading-and-investment agent; uses the persona as the main interaction style.
- [liangdabiao/autogen-financial-analysis](https://github.com/liangdabiao/autogen-financial-analysis) - Microsoft AutoGen-based multi-agent financial-analysis system; VaR / Monte Carlo / factor models / visualization integration.

> [!NOTE]
> Also useful here: [guangxiangdebizi/TradingAgents-MCPmode](#mcps-tradingagents-mcpmode) turns TradingAgents-style research into MCP tools. The full entry is in MCPs · Research tools / analysis.

> Also see: [chrisworsey55/atlas-gic](#agents-atlas-gic) is listed under single-agent traders, but it is relevant here because it replaces debate with continuous self-research.

<a id="agents-single-agent"></a>
### Single-agent end-to-end traders

<a id="agents-ai-hedge-fund"></a>
- [virattt/ai-hedge-fund](https://github.com/virattt/ai-hedge-fund) - Widely forked LLM-driven equity-trading repo; analyst personas (Buffett / Munger / Cathie Wood) propose, the portfolio manager decides.
- [TraderAlice/OpenAlice](https://github.com/TraderAlice/OpenAlice) - "Your one-person Wall Street"; single agent covering research → entry → hold → exit; Claude Agent SDK + Trading-as-Git approval workflow + cross-asset UTA account design.
<a id="agents-atlas-gic"></a>
- [chrisworsey55/atlas-gic](https://github.com/chrisworsey55/atlas-gic) - General Intelligence Capital's self-improving trading agent; focuses on continuous self-research rather than agent debate.
- [Gajesh2007/ai-trading-agent](https://github.com/Gajesh2007/ai-trading-agent) - AI trading agent on Hyperliquid; single-LLM-driven execution; shows direct Hyperliquid integration.
- [kweinmeister/agentic-trading](https://github.com/kweinmeister/agentic-trading) - Trading-workflow example built on Google ADK + A2A interop; an alternative implementation outside LangGraph.
- [danilobatson/ai-trading-agent-gemini](https://github.com/danilobatson/ai-trading-agent-gemini) - LunarCrush social-sentiment + Google Gemini crypto-trading agent; built with Next.js 15, Inngest, and Supabase.
- [alsk1992/CloddsBot](https://github.com/alsk1992/CloddsBot) - Open-source AI trader across 1000+ markets, including Polymarket, Kalshi, Binance, Hyperliquid, Solana, and several EVM chains.
- [hkirat/ai-trading-agent](https://github.com/hkirat/ai-trading-agent) - "Trade using LLMs"; minimal TypeScript demo from Harkirat Singh; common on-ramp for TS learners.

<a id="agents-research-copilots"></a>
### Research / equity-research copilots

- [ZhuLinsen/daily_stock_analysis](https://github.com/ZhuLinsen/daily_stock_analysis) - Daily LLM-driven stock-screening dashboard; multi-channel push (WeChat / Feishu / Telegram / Discord / Slack / email); 11 built-in strategies + agent stock-Q&A; deploy-by-GitHub-Actions.
- [AmadeusGB/alpha-arena](https://github.com/AmadeusGB/alpha-arena) - Live AI-agent competition and research platform; uses real-market conditions to improve agents.
- [TNT-Likely/PanWatch](https://github.com/TNT-Likely/PanWatch) - PanWatch / "盯盘侠"; AI-driven stock-monitoring assistant; multi-account positions + agent analysis + PWA mobile.
- [rnikitin/QuantGPT](https://github.com/rnikitin/QuantGPT) - AI co-pilot for quant traders and researchers; early project from 2023, still maintained.
- [HKUSTDial/DeepEar](https://github.com/HKUSTDial/DeepEar) - DeepEar / "顺风耳"; HKUST-Dial Lab's open-source deep-research and signal-tracking framework; joint multimodal news + price tracking.
- [kamathhrishi/finance-agent](https://github.com/kamathhrishi/finance-agent) - Earnings-call / SEC-filing / news Q&A agent; clean RAG-over-disclosures implementation.

> Also relevant: [ginlix-ai/LangAlpha](#agents-langalpha) and [oficcejo/aiagents-stock](#agents-tradingagents) both include research-copilot screens, but their main entries stay with the multi-agent systems they belong to.

<a id="agents-real-money"></a>
### Real-money / competition experiments

<a id="agents-llm-trading-lab"></a>
- [LuckyOne7777/LLM-Trading-Lab](https://github.com/LuckyOne7777/LLM-Trading-Lab) - Real-money six-month experiment; ChatGPT manages a real US-equity micro-cap portfolio under strict pre-defined rules; ships with a 40-page evaluation paper.
- [195440/nof1.ai](https://github.com/195440/nof1.ai) - Open-source autonomous AI trading agent from the nof1 family; TypeScript port.
- [oficcejo/alpha-arena-okx](https://github.com/oficcejo/alpha-arena-okx) - OKX re-implementation of nof1.ai's Alpha Arena; DeepSeek / Qwen3-Max as decision-makers; useful when comparing Chinese-language nof1 projects.
- [wfnuser/OpenNof1](https://github.com/wfnuser/OpenNof1) - "Your custom 24/7 AI trading agent"; open-source implementation of the nof1.ai Alpha Arena approach.
- [kojott/LLM-trader-test](https://github.com/kojott/LLM-trader-test) - Lightweight teaching testbed for the nof1.ai Alpha Arena approach.

<a id="agents-prediction-market"></a>
### Prediction-market specialists

- [ryanfrigo/kalshi-ai-trading-bot](https://github.com/ryanfrigo/kalshi-ai-trading-bot) - Grok-4-driven Kalshi prediction-market multi-agent trading system; portfolio optimization + 5-gate risk engine.
- [OctagonAI/kalshi-trading-bot-cli](https://github.com/OctagonAI/kalshi-trading-bot-cli) - AI-native CLI for Kalshi and Polymarket; researches an event, estimates probability, then compares it with the live order book.
- [jvnhaoWen/PolyAgent](https://github.com/jvnhaoWen/PolyAgent) - Polymarket-focused multi-skill trading agent; focused single-venue Polymarket LLM agent.

> Also useful here: [agent-next/polymarket-paper-trader](#mcps-polymarket-paper-trader) is listed under MCPs because it is a paper-trading simulator, but it is built for AI agents.

> Also see: [YichengYang-Ethan/oracle3](#agents-oracle3) is listed with multi-agent systems above, and it is especially relevant here for multi-venue prediction-market arbitrage.

<a id="agents-benchmarks"></a>
### Benchmarks & evaluations

- [ulab-uiuc/live-trade-bench](https://github.com/ulab-uiuc/live-trade-bench) - Live-market evaluation for trading agents; UIUC ULab's live-eval benchmark; distinct from backtest-only benchmarks.
- [Open-Finance-Lab/AgenticTrading](https://github.com/Open-Finance-Lab/AgenticTrading) - Open-Finance-Lab's academic framework + dataset for agent-trading research.
- [vals-ai/finance-agent](https://github.com/vals-ai/finance-agent) - Finance-agent benchmark / task suite from vals-ai.

<a id="agents-strategy-coding"></a>
### Strategy coding / self-improving agents

- [paperswithbacktest/pwb-alphaevolve](https://github.com/paperswithbacktest/pwb-alphaevolve) - DeepMind AlphaEvolve-style agent that uses an LLM to write and improve trading strategies for backtesting.

> Note: [`TauricResearch/Trading-R1`](https://github.com/TauricResearch/Trading-R1) is not listed yet because its terminal has not launched. It can be added once the project is publicly usable.

<a id="mcps"></a>
## MCPs

<p align="center">
  <img src="assets/section-mcps.png" alt="MCPs section header" width="760" />
</p>

MCPs are servers that let an agent call external tools through the Model Context Protocol. In this list, they mostly cover market data, broker or exchange actions, research tools, and backtesting services.

> [!NOTE]
> Same author to compare: `guangxiangdebizi/` maintains [FinanceMCP](#mcps-financemcp) for data access and [TradingAgents-MCPmode](#mcps-tradingagents-mcpmode) for TradingAgents-style research tools. They solve different problems, so they stay in separate sections.

<a id="mcps-market-data"></a>
### Market data / data providers

<a id="mcps-financial-datasets"></a>
- [financial-datasets/mcp-server](https://github.com/financial-datasets/mcp-server) - Financial Datasets' first-party MCP; US-equity + crypto fundamentals (3 statements + ratios) + prices + news.
- [6551Team/opennews-mcp](https://github.com/6551Team/opennews-mcp) - 84+ news-source aggregation (Bloomberg / Reuters / FT / CoinDesk and more) + AI impact-scoring / trading-signal + WebSocket streaming.
- [BlockRunAI/blockrun-mcp](https://github.com/BlockRunAI/blockrun-mcp) - Real-time data MCP with pay-per-call x402 payments; covers search, research, quotes, crypto, X, and Twitter.
<a id="mcps-financemcp"></a>
- [guangxiangdebizi/FinanceMCP](https://github.com/guangxiangdebizi/FinanceMCP) - Tushare + Binance MCP spanning A-shares / HK / US / funds / bonds / macro / stablecoins / crypto / financial news.
- [saidsurucu/borsa-mcp](https://github.com/saidsurucu/borsa-mcp) - Turkish BIST + US-equity + fund data MCP serving regional markets outside China and the US.
- [aahl/mcp-aktools](https://github.com/aahl/mcp-aktools) - Stock and crypto data MCP built on akshare / aktools; broad market-data coverage through the AKShare ecosystem.
- [elsejj/mcp-cn-a-stock](https://github.com/elsejj/mcp-cn-a-stock) - A-share-only data MCP; single-market deep coverage instead of multi-source aggregation.
- [massive-com/mcp_massive](https://github.com/massive-com/mcp_massive) - Massive (formerly Polygon.io) first-party MCP; multi-asset market-data coverage.
- [Alex2Yang97/yahoo-finance-mcp](https://github.com/Alex2Yang97/yahoo-finance-mcp) - Full-feature Yahoo Finance MCP; historical prices + fundamentals + option chains + news; Yahoo wrapper.
- [stefanoamorelli/sec-edgar-mcp](https://github.com/stefanoamorelli/sec-edgar-mcp) - SEC EDGAR MCP; 10-K / 10-Q / 8-K / insider trades / filings reader; common filings entry across awesome-lists.
- [zwldarren/akshare-one-mcp](https://github.com/zwldarren/akshare-one-mcp) - A-share data MCP backed by the AKShare-One normalizer; an alternative implementation within the AKShare ecosystem.
- [imbenrabi/Financial-Modeling-Prep-MCP-Server](https://github.com/imbenrabi/Financial-Modeling-Prep-MCP-Server) - FMP MCP with 250+ tools for fundamentals, market intelligence, and ETFs.
- [narumiruna/yfinance-mcp](https://github.com/narumiruna/yfinance-mcp) - Minimal yfinance MCP; a lightweight Yahoo Finance data option.
- [OctagonAI/octagon-mcp-server](https://github.com/OctagonAI/octagon-mcp-server) - MCP for filings, earnings calls, financials, stock data, private-market deals, and web research.

<a id="mcps-brokerage"></a>
### Brokerage / exchange trading

<a id="mcps-alpaca"></a>
- [alpacahq/alpaca-mcp-server](https://github.com/alpacahq/alpaca-mcp-server) - Alpaca's official MCP for market data plus paper or live trading in equities, ETFs, options, and crypto. *(← used by: [tradermonty/claude-trading-skills](#skills-claude-trading-skills), [staskh/trading_skills](#skills-trading-skills), [huygiatrng/AlpacaTradingAgent](#agents-tradingagents).)*
<a id="mcps-kraken-cli"></a>
- [krakenfx/kraken-cli](https://github.com/krakenfx/kraken-cli) - Kraken's official AI-native CLI with an embedded MCP; covers crypto, xStocks, forex, derivatives, paper trading, and bundled SKILL.md packs.
<a id="mcps-koreainvestment"></a>
- [koreainvestment/open-trading-api](https://github.com/koreainvestment/open-trading-api) - Korea Investment & Securities official SDK; includes a Trading MCP, strategy builder, and backtester.
- [okx/agent-trade-kit](https://github.com/okx/agent-trade-kit) - OKX official MCP for spot, perpetuals, futures, options, and grid bots.
- [ariadng/metatrader-mcp-server](https://github.com/ariadng/metatrader-mcp-server) - Representative MT5 MCP; lets LLMs trade through any MetaTrader 5 broker; MCP connector for a major retail-forex platform.
- [Qoyyuum/mcp-metatrader5-server](https://github.com/Qoyyuum/mcp-metatrader5-server) - Alternative MT5 MCP for quotes, trading, and history; uses MCP resources as well as tools.
- [rcontesti/IB_MCP](https://github.com/rcontesti/IB_MCP) - Representative IBKR MCP; exposes Interactive Brokers TWS / Gateway as MCP tools; aimed at professional-broker workflows.
- [code-rabi/interactive-brokers-mcp](https://github.com/code-rabi/interactive-brokers-mcp) - Alternative IBKR MCP in TS / JS; complements rcontesti's Python build.
- [taylorwilsdon/quantconnect-mcp](https://github.com/taylorwilsdon/quantconnect-mcp) - Independent QuantConnect MCP focused on strategy research and workflow automation.

> Also useful for Skills readers: [krakenfx/kraken-cli](#mcps-kraken-cli) includes 50 bundled SKILL.md packages. The main entry is here because it is primarily an exchange trading tool.

<a id="mcps-research-tools"></a>
### Research tools / analysis

- [wshobson/maverick-mcp](https://github.com/wshobson/maverick-mcp) - Personal stock-analysis MCP for fundamentals, technical indicators, and screening.
<a id="mcps-tradingagents-mcpmode"></a>
- [guangxiangdebizi/TradingAgents-MCPmode](https://github.com/guangxiangdebizi/TradingAgents-MCPmode) - TradingAgents refactored as MCP tools for multi-agent equity research.
- [QuantMLResearch/AI-Kline](https://github.com/QuantMLResearch/AI-Kline) - Stock-analysis tool combining classic technical analysis, AI prediction, and MCP access.
- [wbsu2003/stock-scanner-mcp](https://github.com/wbsu2003/stock-scanner-mcp) - Stock scanner MCP for prices, scoring, technical reports, and AI summaries.

> Also relevant: [dragon1086/prism-insight](#agents-prism-insight) is listed under Agents; this section mentions it because it has built-in MCP support for research.

<a id="mcps-tradingview"></a>
### TradingView bridge

- [atilaahmettaner/tradingview-mcp](https://github.com/atilaahmettaner/tradingview-mcp) - 30+-tool TradingView MCP; 6 backtest strategies + Reddit sentiment + news + multi-exchange; many tools work without an API key.

<a id="mcps-prediction-market"></a>
### Prediction markets

<a id="mcps-polymarket"></a>
- [caiovicentino/polymarket-mcp-server](https://github.com/caiovicentino/polymarket-mcp-server) - 45-tool Polymarket MCP; real-time monitoring and explicit order-safety guards.
<a id="mcps-polymarket-paper-trader"></a>
- [agent-next/polymarket-paper-trader](https://github.com/agent-next/polymarket-paper-trader) - Polymarket paper-trading simulator; MCP server + real-time order book + strategy backtesting; built for AI agents.

<a id="mcps-backtesting"></a>
### Strategy / backtesting platforms

- [whchien/ai-trader](https://github.com/whchien/ai-trader) - Backtrader-based framework with 20+ strategies, multi-market support, CLI tools, and an embedded MCP for agent workflows.

<a id="skills"></a>
## Skills

<p align="center">
  <img src="assets/section-skills.png" alt="Skills section header" width="760" />
</p>

Skills are reusable instructions and workflows for Claude Code or other agent systems. They help an agent repeat a trading task reliably, such as researching a stock, checking options, backtesting a strategy, or managing a portfolio. When a Skill is designed to work with a listed MCP, the entry shows `→ pairs with`.

<a id="skills-equity-research"></a>
### Equity research

<a id="skills-claude-trading-skills"></a>
- [tradermonty/claude-trading-skills](https://github.com/tradermonty/claude-trading-skills) - Large Skill pack for US-equity investors, covering market analysis, breadth, regimes, screening methods, options, Alpaca portfolio management, and research workflows. *(→ pairs with: [alpacahq/alpaca-mcp-server](#mcps-alpaca).)*
<a id="skills-finance-skills"></a>
- [himself65/finance-skills](https://github.com/himself65/finance-skills) - Skill pack for multiple asset classes, covering valuation, earnings review, option payoffs, ETF checks, liquidity, social research, and geopolitical-risk analysis.
- [quant-sentiment-ai/claude-equity-research](https://github.com/quant-sentiment-ai/claude-equity-research) - Claude Code research Skill for buy / sell / hold reports using fundamentals, technicals, option flow, insider activity, and sector context.
<a id="skills-alphaear"></a>
- [RKiding/Awesome-finance-skills](https://github.com/RKiding/Awesome-finance-skills) - Alphaear Skill suite for news, stocks, sentiment, prediction, signal tracking, logic visualization, reporting, and search.

> Also useful here: [HKUDS/Vibe-Trading](#agents-vibe-trading) and [ginlix-ai/LangAlpha](#agents-langalpha) both include bundled Skills. Their main entries stay under Agents because they are full agent workspaces, not just Skill packs.

<a id="skills-crypto"></a>
### Crypto / DeFi / on-chain

- [okx/onchainos-skills](https://github.com/okx/onchainos-skills) - OKX official Skills for OnchainOS, covering wallets, token discovery, quotes, DEX swaps, and transaction broadcasting.
- [okx/agent-skills](https://github.com/okx/agent-skills) - OKX bilingual Skills repo with contribution, review, and security guidance; companion to onchainos-skills.

<a id="skills-strategy-coding"></a>
### Strategy coding & backtesting

<a id="skills-vectorbt-backtesting"></a>
- [marketcalls/vectorbt-backtesting-skills](https://github.com/marketcalls/vectorbt-backtesting-skills) - Skill for vectorbt backtesting with setup, backtest, optimization, quick stats, strategy comparison, and reusable strategy templates.

<a id="skills-brokerage"></a>
### Brokerage execution & portfolio

<a id="skills-trading-skills"></a>
- [staskh/trading_skills](https://github.com/staskh/trading_skills) - Skill pack for option traders, covering market data, analysis, scanners, portfolio work, reports, IBKR integration, and MCP tools. *(→ pairs with: [alpacahq/alpaca-mcp-server](#mcps-alpaca), [rcontesti/IB_MCP](https://github.com/rcontesti/IB_MCP).)*
- [koreal6803/finlab-ai](https://github.com/koreal6803/finlab-ai) - Taiwan-equity CLI Skill for strategy discovery, backtesting, and feature engineering with FinLab data and ready-made strategy examples.

> Also useful here: [krakenfx/kraken-cli](#mcps-kraken-cli) includes SKILL.md packages for crypto, xStocks, forex, and derivatives. The full entry is under MCPs because Kraken CLI is mainly an exchange trading tool.

<a id="resources"></a>
## Resources

<a id="resources-papers"></a>
### Papers

> Included here: papers that directly introduce or explain a project listed here. For a broader finance-LLM paper, model, and dataset list, see [`DataArcTech/Awesome-FinLLMs`](https://github.com/DataArcTech/Awesome-FinLLMs).

- [TradingAgents: Multi-Agents LLM Financial Trading Framework](https://arxiv.org/abs/2412.20138) - Tauric Research team, arXiv 2412.20138 (2024). Introduces the multi-agent debate decision framework: analyst team + bull/bear researcher debate + trader + risk control + portfolio manager. [paper](https://arxiv.org/abs/2412.20138) · [code](#agents-tradingagents)
- [LLM-Trading-Lab: Six-Month Real-Money ChatGPT Micro-Cap Experiment](https://github.com/LuckyOne7777/LLM-Trading-Lab) - Lucky One, 2025; ships with a 40-page evaluation paper. Forward-only audit of ChatGPT managing a real US-equity micro-cap portfolio for six months under strict pre-defined rules. [paper / repo](https://github.com/LuckyOne7777/LLM-Trading-Lab) · [code](#agents-llm-trading-lab)
- [FinRobot: Open-Source AI Agent Platform for Financial Analysis](https://arxiv.org/abs/2405.14767) - AI4Finance Foundation, arXiv 2405.14767 (2024). Early academic finance-AI agent platform; multimodal analyst agents tied to the FinGPT model line. [paper](https://arxiv.org/abs/2405.14767) · [code](https://github.com/AI4Finance-Foundation/FinRobot)

> For broader finance-LLM papers, models, and datasets, see [`DataArcTech/Awesome-FinLLMs`](https://github.com/DataArcTech/Awesome-FinLLMs). This list stays focused on usable agent, MCP, and Skill projects.

<a id="resources-learn"></a>
### Learn

> Included here: public talks, courses, and long-form posts about LLM-driven trading. We skip generic LLM tutorials, generic finance tutorials, and paid courses without a public artifact.

- [Tauric Research GitHub Org](https://github.com/TauricResearch) - Tauric Research, ongoing 2024–2026. Official org behind the TradingAgents framework; public README / docs / companion technical reports (arXiv 2412.20138 / 2509.11420); a good place to learn how multi-agent trading systems are built. [link](https://github.com/TauricResearch)
- [AI4Finance Foundation GitHub Org](https://github.com/AI4Finance-Foundation) - AI4Finance Foundation, ongoing 2022–2026. Official org behind the FinRobot / FinGPT / FinRL line; ProjectShare / tutorial notebooks / paper companion code; a good place to learn academic finance-AI agents. [link](https://github.com/AI4Finance-Foundation)

> Note: the v0.1 Learn section is intentionally short. Future updates can add talks, courses, podcasts, and conference sessions as they become useful to readers.

<a id="contributing"></a>
## Contributing

We welcome community contributions: new entries, removal of dead links, and discussion on sub-category boundaries. Start with [CONTRIBUTING.md](CONTRIBUTING.md) (or [CONTRIBUTING.zh-CN.md](CONTRIBUTING.zh-CN.md) in Chinese); the guide puts the AI-native review path, quality bar, submission format, `awesome-lint` check, and bilingual-PR rule in one place. New entries are smoothest via the [Issue: add entry](.github/ISSUE_TEMPLATE/add-entry.md) template; removals via the [Issue: remove entry](.github/ISSUE_TEMPLATE/remove-entry.md) template.

<a id="related-awesome-lists"></a>
## Related awesome lists

- [DataArcTech/Awesome-FinLLMs](https://github.com/DataArcTech/Awesome-FinLLMs) - Comprehensive finance-LLM paper / model / dataset list (complementary to this list — they cover base models and papers, we cover the application-layer agents · MCPs · Skills).
- [punkpeye/awesome-mcp-servers](https://github.com/punkpeye/awesome-mcp-servers) - Broad MCP server directory; use this list when you only want trading, research, data, and execution tools.
- [georgezouq/awesome-ai-in-finance](https://github.com/georgezouq/awesome-ai-in-finance) - Traditional AI-in-finance list for deep learning, reinforcement learning, and time-series work.
- [wilsonfreitas/awesome-quant](https://github.com/wilsonfreitas/awesome-quant) - Classical quant-library list; useful, but not the focus here.
- [wangzhe3224/awesome-systematic-trading](https://github.com/wangzhe3224/awesome-systematic-trading) - Systematic-trading list for the broader non-agent trading tools.

<a id="maintained-by"></a>
## Maintained by

<div align="center">
  <img src="assets/llmquant-logo.svg" alt="LLMQuant" width="72" />
  <br/>
  <strong><a href="https://llmquant.com">LLMQuant</a></strong>
  <br/>
  <sub>Open-source community for AI, LLMs, and quantitative finance.</sub>
  <br/><br/>
  <a href="https://llmquant.com">Website</a> ·
  <a href="https://github.com/LLMQuant">GitHub</a> ·
  <a href="https://linkedin.com/company/llmquant">LinkedIn</a>
</div>

The maintainer team reviews new entries and category changes.
