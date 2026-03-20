---
name: cc-connect-send
description: Send message, files or images to Feishu/Telegram via cc-connect. Use when the user wants to send a generated file, report, chart, or image to their messaging platform (Feishu, Telegram, etc.).
---

# CC-Connect Send

When the user wants to send message, file or image to their messaging platform:

```bash
Send a message or attachment to an active cc-connect session.

Options:
  -m, --message <text>     Message to send (preferred over positional args)
      --image <path>       Send an image attachment (repeatable)
      --file <path>        Send a file attachment (repeatable)
      --stdin              Read message from stdin (best for long/special-char messages)
  -p, --project <name>     Target project (optional if only one project)
  -s, --session <key>      Target session key (optional, picks first active)
      --data-dir <path>    Data directory (default: ~/.cc-connect)
  -h, --help               Show this help

Examples:
  cc-connect send "Daily summary: ..."
  cc-connect send -m "Build completed successfully"
  cc-connect send --message "Chart generated" --image /tmp/chart.png
  cc-connect send --file /tmp/report.pdf
  cc-connect send --stdin <<'EOF'
    Long message with "special" chars, $variables, and newlines
  EOF
