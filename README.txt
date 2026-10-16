SLEEPING BARBER — FINAL BROWSER SIMULATION

How to run
1. Extract this ZIP file.
2. Open Sleeping_Barber_Final/index.html in Safari, Chrome, or Firefox.
3. Choose Traditional semaphore model or Modified FIFO.
4. Set the same inputs for each version, then click Reset and Start.
5. Compare the service order and individual customer results table.

What the two modes demonstrate
- Traditional semaphore model: an illustrative non-FIFO wake-up example that selects the newest waiting customer first. This demonstrates that a semaphore does not itself promise FIFO fairness; it is not a claim that every real semaphore behaves this way.
- Modified FIFO: an explicit FIFO queue selects the oldest waiting customer first.
- The number turned away can be the same because both modes use the same waiting-room capacity.
- Average waiting time can also match for some settings. The service order and per-customer wait table are the primary evidence of the ordering difference.

Model scope and limitations
This is a deterministic browser simulation of the concept. Semaphore indicators are explanatory state indicators, not live POSIX sem_t values or actual pthread synchronization. The traditional non-FIFO order is deliberately illustrative so the fairness contrast can be observed. It should not be described as a live POSIX implementation.

Validation performed
- JavaScript syntax checked with Node.js.
- Simulation logic checked against several input cases: zero waiting chairs, one customer, sustained arrivals, and spaced arrivals.
- Inputs are validated as integers within the displayed limits.
- The Step control resets the model when any configuration input changes.
