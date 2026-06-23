# Design

## Overview

The portfolio uses a "technical atlas" visual system: quiet neutral surfaces, precise rulework, project media as the hero material, and compact evidence blocks. It is a brand site for cloud/backend recruiting, not an app dashboard and not a generic resume page.

## Color

- Light theme: cool off-white background, deep green-black ink, pale mint surfaces, teal action color, and a restrained amber signal accent.
- Dark theme: graphite green-black background, soft mint-tinted text, dark panels, teal action color, and muted amber highlights.
- Use OKLCH tokens in CSS for palette control. Body text must meet WCAG AA; muted text should stay readable and never fall into low-contrast decorative gray.

## Typography

- Use Sora as the single type family across display, body, navigation, and UI. The page relies on scale and weight contrast rather than a decorative font pairing.
- Display headings use tight but safe spacing, never below `-0.04em`.
- Body copy should stay within 65-75 characters where possible and use comfortable line-height for scanning.

## Layout

- Narrative order is hero, projects, experience, skills, certificates, contact.
- Hero is split between hiring pitch and project-media atlas panel.
- Projects are the main proof surface and should feel more substantial than supporting sections.
- Supporting sections use ruled panels and compact blocks instead of a long run of identical cards.
- Mobile layouts stack without horizontal overflow, preserve readable controls, and keep project links wrapped.

## Components

- Topbar: sticky, compact, lightly bordered, with navigation ordered around recruiter intent.
- Hero atlas: paired project media and a small profile/status module.
- Project card: media-first proof panel with repo/demo/docs actions, tags, role, and outcome.
- Experience entry: company/logo, role, metrics, and highlights with visible hierarchy.
- Skills carousel: supporting capability map, not the primary story.
- Certificate card: compact verification item that opens the existing PDF modal.
- Contact/CV: conversion area with direct copy and accessible form states.

## Motion

- Content must be visible by default; reveal behavior may add polish but must never gate rendering.
- Project videos use poster-first lazy loading so Safari and Chromium show a useful frame immediately.
- Motion should use short ease-out transitions and respect `prefers-reduced-motion`.
