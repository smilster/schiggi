# schiggi

This is a basic example of how to use a workflow runner to create data and push to the very same GitHub repository. It employs <code>actions/checkout@v4</code> and <code>EndBug/add-and-commit@v9</code>.

The runner controlled by <code>.github/workflows/ffmpeg.yaml</code> starts an <code>ubuntu-latest</code> instance on new <code>*.jpg</code> files in <code>.github/workflows/data/</code>. Inside this instance, in runs <code>ffmpeg</code> in a <code>docker</code> container fetched from <code>lscr.io/linuxserver/ffmpeg:latest</code> and converts all JPEGs into a MP4-video,<code>schiggi.mp4</code>. The result is eventually stored in the root directory of the repository and pushed by <b>github-actions[bot]</b>.
