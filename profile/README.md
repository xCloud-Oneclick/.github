# xCloud-Oneclick

Open-source building blocks behind xCloud's One-Click apps.

This org holds the images, templates and tooling that power the [One-Click apps](https://xcloud.host/one-click-apps/) on [xCloud](https://xcloud.host), a cloud hosting and server-management platform. Everything here is built from open-source upstream projects; licences stay with the upstream projects.

## Repositories

| Repository | What it is |
|---|---|
| [oneclick-images](https://github.com/xCloud-Oneclick/oneclick-images) | Container images for open-source apps that publish no official image: pinned rebuilds of tagged upstream releases, multi-arch, smoke-tested, scanned and signed. |

## Using the images

Images are published to GitHub Container Registry:

```bash
docker pull ghcr.io/xcloud-oneclick/<image>:<upstream-version>-xcloud.<n>
```

Tags are immutable: a rebuild of the same upstream release gets the next `-xcloud.<n>`.

Verify the signed build provenance of an image:

```bash
gh attestation verify oci://ghcr.io/xcloud-oneclick/<image>:<tag> --owner xCloud-Oneclick
```

## Contribute

Open a pull request from a fork of the relevant repository. CI on fork pull requests runs only after a maintainer approves the run; only maintainers can merge.

## Security

Report vulnerabilities through each repository's private vulnerability reporting (Security tab → Report a vulnerability), not a public issue. For images, see the [oneclick-images SECURITY.md](https://github.com/xCloud-Oneclick/oneclick-images/blob/main/SECURITY.md). Vulnerabilities in the upstream apps themselves belong upstream.

## About xCloud

[xcloud.host](https://xcloud.host) · [Browse the One-Click apps](https://xcloud.host/one-click-apps/)
