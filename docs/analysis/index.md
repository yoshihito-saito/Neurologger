# Analysis

Analysis documentation covers conversion from WILD exports to analysis-ready files, with timing metadata, MATLAB and Python workflows, and spike-sorting preparation kept explicit.

## Entry Points

<div class="wild-grid">
  <a class="wild-card wild-card-link" href="python/">
    <h3>Python</h3>
    <p>Camera decoding, video/audio handling, GPIO logging, and pipeline integration scripts.</p>
  </a>
  <a class="wild-card wild-card-link" href="matlab/">
    <h3>MATLAB</h3>
    <p>Header generation, preprocessing, IMU processing, and compatibility with existing lab scripts.</p>
  </a>
  <a class="wild-card wild-card-link" href="spike-sorting/">
    <h3>Spike Sorting</h3>
    <p>Recording layouts compatible with common spike-sorting pipelines.</p>
  </a>
</div>

## Reproducibility Checklist

- Record release image filename.
- Record WILD_console version.
- Preserve the raw export folder.
- Preserve the WILD parameter binary.
- Record probe, channel map, sampling rate, and stimulation configuration.
- Track post-processing script version or commit hash.
