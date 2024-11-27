# vite pnpm ssh+git bug

Pnpm use git clone to download package which starts with `git+ssh` and could not be downloaded with tarball, this will
create a local dependency folder with hash like
`.pnpm/blank-package@git+https+++gitclone.com+github.com+lcjnil+blank-package#4c6d7d711b9d2d8ea1a7ea2d22a522d190a7f120`,
and vite will not be able to resolve the dependency.
