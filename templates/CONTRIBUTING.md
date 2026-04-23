# Contributing Guide

Thank you for contributing.

## Workflow
1. Fork the repository
2. Create a branch: `feature/<short-name>` or `fix/<short-name>`
3. Make focused changes
4. Run build/tests locally
5. Open a pull request

## Development Standards
- Keep changes scoped and reviewable
- Follow existing naming conventions and coding style
- Update documentation for behavior changes
- Avoid unrelated refactors in the same PR

## Commit Convention
Use Conventional Commits:
- `feat: add UART ring buffer`
- `fix: handle I2C bus timeout`
- `docs: update flashing instructions`

## Pull Request Checklist
- [ ] Build succeeds
- [ ] Tests pass
- [ ] Docs updated
- [ ] No secrets committed
- [ ] Scope is focused

## Reporting Issues
Use the issue templates and provide:
- Hardware and firmware version
- Steps to reproduce
- Expected vs actual behavior
- Logs / serial output
