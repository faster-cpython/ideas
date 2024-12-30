# Papers

## JIT Compilers

* Deegen: A JIT-Capable VM Generator for Dynamic Languages.
  By Haoran Xu and Fredrik Kjolstad.
  https://arxiv.org/abs/2411.11469

* CacheIR: The Benefits of a Structured Representation for Inline Caches.
  By Jan de Mooij, Matthew Gaudet, Iain Ireland, Nathan Henderson, and J. Nelson Amaral.
  https://dl.acm.org/doi/10.1145/3617651.3622979

* Copy-and-Patch Compilation.
  By Haoran Xu and Fredrik Kjolstad.
  https://arxiv.org/pdf/2011.13127

* PHP RFC: JIT
  By Dmitry Stogov and Zeev Suraski.
  https://wiki.php.net/rfc/jit

* IR JIT Framework a base for the next generation JIT for PHP
  By Dmitry Stogov
  Note: PHP JIT has both tracing and function-based architectures.
  https://www.researchgate.net/publication/374470404_IR_JIT_Framework_a_base_for_the_next_generation_JIT_for_PHP

## Trace-like Architectures

* Simple and Effective Type Check Removal through Lazy Basic Block Versioning.
  By Maxime Chevalier-Boisvert and Marc Feeley.
  https://arxiv.org/pdf/1411.0352

* The HipHop Virtual Machine.
  By Keith Adams, Jason Evans, Bertrand Maher, Guilherme Ottoni, Drew Paroski, Brett Simmers, Edwin Smith, Owen Yamauchi
  https://research.facebook.com/publications/the-hiphop-virtual-machine/

* Tracing the meta-level: PyPy's tracing JIT compiler
  By Carl Friedrich Bolz, Antonio Cuni, Maciej Fijalkowski, and Armin Rigo.
  https://dl.acm.org/doi/10.1145/1565824.1565827


## Specific Compiler Optimizations

* How the Cinder JIT’s function inliner helps us optimize Instagram.
  By Max Bernstein.
  https://engineering.fb.com/2022/05/02/open-source/cinder-jits-instagram/

* Allocation removal by partial evaluation in a tracing JIT.
  Carl Friedrich Bolz, Antonio Cuni, Maciej FijaBkowski, Michael Leuschel, Samuele Pedroni, and Armin Rigo.
  https://dl.acm.org/doi/10.1145/1929501.1929508

* Threaded Code Generation with a Meta-Tracing JIT Compiler.
  By Yusuke Izawa, Hidehiko Masuhara, Carl Friedrich Bolz-Tereick, Youyou Cong.
  https://arxiv.org/abs/2106.12496

## Optimizing Interpreters

* Cross Module Quickening - The Curious Case of C Extensions.
  By Felix Berlakovich and Stefan Brunthaler.
  https://drops.dagstuhl.de/entities/document/10.4230/LIPIcs.ECOOP.2024.6

* Inline caching meets Quickening.
  By Stefan Brunthaler.
  https://www.complang.tuwien.ac.at/kps09/pdfs/brunthaler.pdf


## Benchmarking and Analyzing Python's Overhead
* Python meets JIT compilers: A simple implementation and a comparative evaluation.
  By Qiang Zhang, Lei Xu, Baowen Xu.
  https://doi.org/10.1002/spe.3267

* Quantifying the interpretation overhead of Python.
  By Qiang Zhang, Lei Xu, Xiangyu Zhang, Baowen Xu.
  https://www.sciencedirect.com/science/article/abs/pii/S0167642321001520

* Python Interpreter Performance Deconstructed.
  By Gergö Barany.
  https://www.complang.tuwien.ac.at/gergo/papers/dyla14.pdf


## DSLs
* An Executable Semantics for Faster Development of Optimizing Python Compilers.
  By Olivier Melançon, Marc Feeley, and Manuel Serrano.
  https://www.iro.umontreal.ca/~feeley/papers/MelanconFeeleySerranoSLE23.pdf

* Vmgen—a generator of efficient virtual machine interpreters
  By M. Anton Ertl, David Gregg, Andreas Krall, Bernd Paysan
  https://onlinelibrary.wiley.com/doi/abs/10.1002/spe.434

* PHP RFC: A new JIT implementation based on IR Framework
  https://wiki.php.net/rfc/jit-ir
