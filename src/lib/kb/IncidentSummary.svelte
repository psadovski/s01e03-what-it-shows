<script lang="ts">
  import summary from '#lib/data/incident-4471-summary.json';
</script>

<p><strong>{summary.uniqueReports}</strong> unique reports · <strong>{summary.causes.length}</strong> causes</p>

<table>
  <thead><tr><th>problem</th><th>reports</th></tr></thead>
  <tbody>
    {#each summary.causes as cause (cause.key)}
      <tr><td>{cause.label}</td><td>{cause.reports}</td></tr>
    {/each}
  </tbody>
</table>
