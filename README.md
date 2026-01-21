
# Schiggi 🐢

This is a basic example of how to use a GitHub workflow runner to process pushed data utilizing Docker images and Bash scripts, push the results to the same repository, and deploy the repository on GitHub Pages.

The runner, controlled by [<code>.github/workflows/schiggi.yml</code>](https://github.com/smilster/schiggi/blob/main/.github/workflows/schiggi.yml), starts an <code>ubuntu-latest</code> instance on new <code>*.jpg</code> files in the <code>images</code> folder. Ubuntu runs <code>ffmpeg</code> in a <code>docker</code> container, fetched from <code>lscr.io/linuxserver/ffmpeg:latest</code>, and converts all JPEGs into a MP4-video,<code>schiggi.mp4</code>, which is stored in the root directory of this repository. Further, Ubuntu runs Bash scripts, one creating [<code>images.md</code>](https://github.com/smilster/schiggi/blob/main/images.md) displaying all images, the other one updating the date in this <code>README.md</code>. The files <code>schiggi.mp4</code>, <code>images.md</code>, and <code>README.m</code> are commited and pushed by <b>github-actions[bot]</b>. Finally, the runner deploys this repository (GitHub Pages) to make, e.g., the video conveniently acessible:

<b>[smilster.github.io/schiggi/schiggi.mp4](https://smilster.github.io/schiggi/schiggi.mp4)</b><br>
<sub>created on Sat Feb 21 18:01:34 UTC 2026</sub>


##
<b>Example video created on October 17th 2025.</b><br>
<div align="center">
<video src="https://github.com/user-attachments/assets/11ae2c5b-4e5a-4a91-895b-f11296f31a23" type="video/mp4"></video>
</div>


