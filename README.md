# Tailwind Issue Repro

High CPU usage on bad css code. ([#15135](https://github.com/tailwindlabs/tailwindcss/issues/15135))

## Steps

1. Run `pnpm install`
1. Run `pnpm run dev`
1. Monitor the node process CPU, it usually looks like
   ```text
   node <path>/node_modules/.bin/../@tailwindcss/cli/dist/index.mjs -i app.css -o out.css --watch
   ```
1. Uncomment the commented line in `app.css` and save the file.
1. CPU goes to 20%.
