### nginx trace log module
    Rewrite the error log function to automatically add Trace IDs.

#### Trace IDs
    ntm_traceid & ntm_parentid & ntm_currentid
    Error log will ends with " [NGINX-TRACE] traceid: 7a2a867e1dc897340774f7e52867a0fd, currentid: 0b52e431670ff01420a620ab576d2685, parentid: 00000000000000000000000000000000 [NGINX-TRACE-END]"

#### Config
    main_conf directive "http_trace" & no_args

#### X-NTM-Debug
    if the request headers contains "X-NTM-Debug: 1", the log level will be dynamically adjusted to the "NGX_LOG_DEBUG".
