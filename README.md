# Power-Seeking and Optimal Strategy

Single-file interactive notebook distinguishing unilateral control from the ability to achieve an objective. It compares expected benefits, acquisition and maintenance costs, failure risks, and cooperative alternatives across targeted levels of control. Open `index.html` in a browser or publish it with GitHub Pages; there are no runtime dependencies.

The page leads with the utility graph (with optional gross benefit, cost, and cooperation overlays), a marginal-return view, preset comparisons, and a sensitivity heatmap. Numerical summaries sit below the main graph. The mathematical section comes afterward and explains the payoff functions, first-order condition, boundary regimes, comparative statics, and worked baseline.

**Model:** `U(p) = s + (a-c-s)p - (b+d)p²/2`, `p ∈ [0,1]`. Here `p` is targeted unilateral control and `U` is expected utility. The optimum is `p* = clip((a-c-s)/(b+d), 0, 1)` under `a,b,c,d,s≥0` and `b+d>0`. The baseline also satisfies `a>b`, ensuring gross marginal value is positive throughout; the sliders allow cases where that condition fails. Attempting full takeover is optimal iff `a≥b+c+d+s`. The default example `a=9, b=6, c=2, d=10, s=2` has `p*=0.3125` even though additional targeted control has positive gross instrumental value everywhere. The `p*=0.625` example is available as the "Takeover pays, still suboptimal" preset, showing that attempting takeover can beat inaction without being optimal.

Quadratic benefit and cost functions are chosen for tractability: they make marginal payoffs linear and the optimum explicit. They can be interpreted as local second-order approximations, not empirical laws. The underlying distinction between positive gross returns and net-optimal control does not require quadratic functions.

All parameter values are illustrative, not empirical estimates. MathJax SVG equations are pre-rendered and embedded in the HTML so they display correctly offline.

## GitHub Pages

Live site: https://forkhead-box-protein-p2.github.io/power-seeking-model/

Repository: https://github.com/Forkhead-box-protein-P2/power-seeking-model

GitHub Pages publishes the root of the `main` branch. Commit and push changes to update the site. The `.nojekyll` file keeps deployment as plain static HTML; no installation or build is required.
