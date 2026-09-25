# MCP tool surface

The default MapleMCP 0.2.28 public contract exposes **78 tools**.

## Device discovery — 1

`list_devices`

## Desktop/server — 34

`get_config`, `read_file`, `read_multiple_files`, `write_file`, `write_pdf`, `create_directory`, `list_directory`, `move_file`, `copy_path`, `delete_path`, `hash_file`, `get_directory_size`, `get_file_info`, `edit_block`, `start_process`, `read_process_output`, `process_send_input`, `interact_with_process`, `force_terminate`, `list_sessions`, `list_processes`, `process_tree`, `kill_process`, `start_search`, `get_more_search_results`, `stop_search`, `list_searches`, `get_disk_usage`, `get_system_resources`, `list_network_interfaces`, `dns_lookup`, `tcp_probe`, `get_usage_stats`, `get_recent_tool_calls`.

## Browser / ChatGPT-browser — 31

`browser_companion_status`, `browser_companion_update`, `chatgpt_send`, `chatgpt_status`, `chatgpt_cancel`, `chatgpt_ask`, `chatgpt_continue`, `browser_status`, `browser_create_session`, `browser_list_sessions`, `browser_release_session`, `browser_set_visibility`, `browser_list_tabs`, `browser_open_tab`, `browser_close_tab`, `browser_navigate`, `browser_snapshot`, `browser_screenshot`, `browser_click`, `browser_type`, `browser_select`, `browser_press_key`, `browser_back`, `browser_forward`, `browser_wait`, `browser_cookies_read`, `browser_cookies_write`, `browser_storage_state_export`, `browser_devtools_command`, `browser_evaluate`, `browser_network_interception`.

## Mobile — 12

`mobile_get_device_info`, `mobile_launch_app`, `mobile_open_url`, `mobile_media_control`, `mobile_list_notifications`, `mobile_ui_snapshot`, `mobile_ui_screenshot`, `mobile_ui_tap`, `mobile_ui_scroll`, `mobile_ui_global_action`, `mobile_ui_set_text`, `mobile_ui_gesture`.

## Resident worker canary

0.2.28 contains a feature-gated Worker Fabric canary:

`ask_device`, `list_device_workers`, `get_device_worker_task`, `send_device_worker_message`, `pause_device_worker_task`, `resume_device_worker_task`, `cancel_device_worker_task`, `list_device_worker_attention`.

These controls are **not** part of normal 78-tool discovery.

## Capability does not equal permission

Tool discovery describes the global contract. `list_devices` reports the capability policy granted to each enrolled device. Device and execution policy remain authoritative.
