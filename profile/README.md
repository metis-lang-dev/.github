# metis

**LLP** is a small language for behavior catalogs: typed, weighted
linear-logic clauses over finite domains. One catalog, ground per
situation, is read three ways —

- **proof theory** — typing, containment admission, a proof-net normal
  form giving canonical program identity (`program_key`);
- **derivations** — staged multiset rewriting: the space of candidate
  futures, pinned on the wire by a portable seeded reference sampler;
- **denotation** — the induced probability measure: the compiled IR is a
  factor graph with shipped elimination schedules, and exact
  filtering / conditioning / decision scoring is table operations along
  them.

The same catalog that *runs* is the one you can *prove things about*
and *measure exactly* — and when the world surprises it, the loop turns
that surprise back into a gated, human-approved catalog change.

## Repositories

| repo | what it is |
| --- | --- |
| [**metis-lang**](https://github.com/metis-lang-dev/metis-lang) | The language product, self-contained: the OCaml **metisc** compiler (stdlib only, one static binary), the header-only C++17 runtime, the language / IR / canonical-key specs, the parity corpus with committed goldens, and editor tooling (VS Code, Emacs). |
| [**metispy**](https://github.com/metis-lang-dev/metispy) | The python referee + research kit: exact inference, learning (Dirichlet notching, MAP-EM), decision, surprise records + `recover()` replay, and the formalization gate cascade. It referees the shipping toolchain rather than being it. |
| [**metis-catalog**](https://github.com/metis-lang-dev/metis-catalog) | Behavior catalogs with certified artifacts: road world models plus a playground of logical domains — the Ceptre love triangle, Game of Life (IPPC), the Overcooked kitchen — each a full LLP world model gated on metisc goldens. |
| [**metis-loop**](https://github.com/metis-lang-dev/metis-loop) | The explanation / formalization loop: surprise records → mined text → LLM-drafted candidate pack → gate cascade → repair → human-approved catalog change. The REPL is the loop; the CLI and web console are wrappers. |

## The paper

**[Behavior Programs as Measures over Proofs](https://github.com/metis-lang-dev/metis-lang/blob/master/paper/metis.pdf)**
(draft 0.3, 2026-09-30 — [PDF](https://raw.githubusercontent.com/metis-lang-dev/metis-lang/master/paper/metis.pdf) ·
[LaTeX source](https://github.com/metis-lang-dev/metis-lang/blob/master/paper/metis.tex)) —
staged stochastic multiset rewriting with a linear-logic front end, an
MLL^B proof-net IR, and an executable, certified, machine-checked
compilation pipeline. Its central metatheory is machine-checked in
Lean 4: Theorem 3 (equivalence onto the image) in full, and the cores
of Theorems 1, 2 and 4 — see
[`metis-lang/formal/`](https://github.com/metis-lang-dev/metis-lang/tree/master/formal),
sorry-free on Lean's three standard axioms.

## Where to start

Clone [metis-lang](https://github.com/metis-lang-dev/metis-lang) and run
`make check` — it needs only `ocamlopt` (4.14+) and a C++17 compiler,
and reproduces the parity corpus byte-for-byte.
