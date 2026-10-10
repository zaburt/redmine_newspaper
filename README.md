# Newspaper

A newspaper-style Redmine theme (variant of [Paper](https://github.com/zaburt/redmine_paper)): gray
newsprint, black ink, heavy and thin rules, uppercase section bars and
headlines, and a single red spot color.

## Installation

1. Clone this theme ([https://github.com/zaburt/redmine_newspaper](https://github.com/zaburt/redmine_newspaper)) into the Redmine `themes/`
   directory at the application root (Redmine 7+) as `newspaper`:

   ```
   git clone https://github.com/zaburt/redmine_newspaper.git themes/newspaper
   ```

   The result should contain:

   ```
   themes/newspaper/stylesheets/application.css
   ```

   > Note: Redmine 6 and earlier used `public/themes/` instead of `themes/`.

2. Restart Redmine. In production, precompile assets:

   ```
   RAILS_ENV=production bin/rails assets:precompile
   ```

3. Go to `Administration -> Settings -> Display` and select "Newspaper"
   in the "Theme" drop-down list.

## Customize

1. Change `images/logo.svg` for the header logo, `images/logo-login.svg` for
   the login page and `favicon/favicon.svg` for the browser tab icon.
2. The palette is defined inline as hex values in
   `stylesheets/application.css`:

   | Role                       | Color     |
   |----------------------------|-----------|
   | Black ink (text, rules)    | `#111111` |
   | Newsprint sheet / desk     | `#F1EEE3` / `#DAD6CA` |
   | Section bar / hover        | `#E6E2D6` / `#D9D4C4` |
   | Red spot color             | `#B01E1E` |

   The grain and creases are inline SVG/gradients in the "Paper layer"
   section at the end of `stylesheets/application.css`. Headlines, section
   bars and the wiki drop cap are in the "Newspaper layer" section below it.
3. In production, re-run `assets:precompile` after editing any theme file.

## License

Licensed under [GNU GPLv2](LICENSE).

Copyright (c) 2026 Onur Küçük (onur [at] delipenguen.net)
