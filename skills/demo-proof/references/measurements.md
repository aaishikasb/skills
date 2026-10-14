# Measurement claims

Use this reference when a demo makes a performance, accuracy, efficiency, or comparative claim. Request only evidence needed for that claim; optional measurements should not block unrelated conclusions.

## Establish what was measured

Record the evidence source and date/run identifier when available, device/revision, software and model version, precision, input shape, batch size, and relevant runtime configuration. A specification or advertised peak is not an observed result from this setup.

For timing, identify the start and end of the measured interval: model inference, preprocessing, capture-to-result, display, or a complete control loop. Report warmup policy, sample count, aggregation, and whether execution was synchronized where necessary. Derive only what the data supports: a mean cannot establish a percentile, and a short run cannot establish sustained operation.

Reciprocal latency represents sequential throughput only under the stated execution model. Batching, concurrency, dropped frames, and pipelining can make throughput and per-item latency differ. Keep model timing separate from end-to-end timing.

For sustained or energy claims, inspect run duration and available thermal, clock, utilization, power, and power-mode evidence relevant to the claim. Separate board, accelerator, and whole-system power. Mark estimated values and assumptions; do not imply a power measurement from latency alone.

## Accuracy and comparison

Identify the dataset or input selection, ground truth, metric, sample count, and evaluation procedure. One successful demonstration is evidence for that instance, not a measured accuracy rate. Hardware timing alone does not establish task quality.

Compare runs only after explaining material differences in input, model, precision, batching, timing boundary, device configuration, and quality target. If conditions differ, qualify the comparison instead of attributing the entire difference to the hardware or optimization.

## Rewrite to the evidence

Prefer the narrow supported claim and the next useful measurement. For example, an attributed desktop inference log supports a statement about that desktop run. It does not establish camera-to-output latency on an edge device. Avoid converting missing logs into a claim that the device failed.
