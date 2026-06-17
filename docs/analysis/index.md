# Analysis

Analysis documentation covers conversion from WILD exports to analysis-ready files, with timing metadata, MATLAB and Python workflows, and spike-sorting preparation kept explicit.

## Entry Points

<div class="wild-grid wild-nav-grid">
  <a class="wild-card wild-card-link wild-card-compact" href="python/">
    <div>
    <h3>Python</h3>
      <p>Video and GPIO</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="matlab/">
    <div>
    <h3>MATLAB</h3>
      <p>Preprocessing</p>
    </div>
  </a>
  <a class="wild-card wild-card-link wild-card-compact" href="spike-sorting/">
    <div>
      <h3>Spike sorting</h3>
      <p>Ephys pipeline</p>
    </div>
  </a>
</div>

## Reproducibility Checklist

- Record release image filename.
- Record WILD_console version.
- Preserve the raw export folder.
- Preserve the WILD parameter binary.
- Record probe, channel map, sampling rate, and stimulation configuration.
- Track post-processing script version or commit hash.
