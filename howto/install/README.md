# install

A fresh machine to the workbench: the local manager, its docs mrepo and Splectral in service, by one deploy.

Pattern: commission

The `haicc` command is installed and its sources linked
(`base-linux-haicc`, the how-to `install`). The boot mrepo is put in
place, then the workbench deployed at `workbench`, `local/workbench`. Its
runtime, as it starts, runs its `commission`, and the deploy waits for
it: the workbench's components deployed below it (`workbench/docs`,
`workbench/splectral`), each commissioned by its own, then the workbench
itself initialised and started.

## Steps

The boot mrepo is put in place first, `haicc boot/deploy`, at the machine (`base-component-boot`, the how-to `boot`); the rest is a run.

The script, [steps.haicc](steps.haicc): each line as typed after `haicc`, what it answers under it; run with `howto/run`, shown here at info extraction.

## Notes

- **The host's role**: the workbench is the local manager, its list the
  haicc component's packages; swarms and their nodes are deployed in it
  as in a host.
- **Once on an install**: a second one's commission stops at its first
  component, `in the way`: their unique URIs (`local/docs`) are the
  install's; nothing of the second is left.
- **What runs it**: the commission is a hook, the mrepo's own lines; a
  line that fails fails the deploy, saying which.
