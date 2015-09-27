谁写哪个章节，大家在相应章节目录标记一下 网名+日期。
谁审哪个章节，大家在相应章节目录标记一下 网名(√)。

```
* [Name](#name)     ->      * [Name 某某 2015.8.4](doc/name.md)
* [Name 某某 2015.8.4](doc/name.md)   ->  * [Name 某某 2015.8.4 某某(√)](doc/name.md)
```

章节写好后，存放到`doc`目录下。章节命名用具体小节的锚点名称。例如`Code Repository`章节，存放路径就应是`doc/code-repository.md`。

通过`grep`命令，看以看到更多内部注释信息，方便内部人员进行交流、协作。参考：

```shell
# cd doc
# find *.md | xargs grep "<\!\-\-"

init_by_lua.md:基本上，在这个上下文中，你可以保 。。。<!-- todo wangyuansheng -->
name.md:此模块属第三方扩展，不在Nginx源码中。安装介绍。。。<!-- 超链接没有带 -->
todo.md:<!-- todo 没懂，后面看看怎么翻译  -->
#
```

有任何疑问，可以随时联系我。翻译交流QQ群：435558580 。

Table of Contents
=================

* [Name yuansheng-8.4 moonbingbing(√)](doc/name.md)
* [Status yuansheng-8.6 moonbingbing(√)](doc/status.md)
* [Version](#version)
* [Synopsis yuansheng-8.6](doc/synopsis.md)
* [Description yuansheng-8.16](doc/description.md)
* [Typical Uses yuansheng-8.16](doc/typical-uses.md)
* [Nginx Compatibility yuansheng-8.17](doc/nginx-compatibility.md)
* [Installation yuansheng-8.17](doc/installation.md)
    * [C Macro Configurations yuansheng-8.17 moonbingbing(√)](doc/c-macro-configurations.md)
    * [Installation on Ubuntu 11.10 yuansheng-8.18](doc/installation-on-ubuntu-1110.md)
* [Community](#community)
    * [English Mailing List](#english-mailing-list)
    * [Chinese Mailing List](#chinese-mailing-list)
* [Code Repository yuansheng-8.20 moonbingbing(√)](doc/code-repository.md)
* [Bugs and Patches yuansheng-8.20 moonbingbing(√)](doc/bugs-and-patches.md)
* [Lua/LuaJIT bytecode support yuansheng-8.31](doc/lualuajit-bytecode-support.md)
* [System Environment Variable Support yuansheng-9.1](doc/system-environment-variable-support.md)
* [HTTP 1.0 support lance-2015.8.13](doc/http-10-support.md)
* [Statically Linking Pure Lua Modules yuansheng-9.1](doc/statically-linking-pure-lua-modules.md)
* [Nginx Worker内的数据共享 lance-2015.8.5](doc/data-sharing-within-an-nginx-worker.md)
* [Known Issues](#known-issues)
    * [TCP socket connect operation issues yuansheng-9.2](doc/tcp-socket-connect-operation-issues.md)
    * [Lua Coroutine Yielding/Resuming yuansheng-9.2](doc/lua-coroutine-yieldingresuming.md)
    * [Lua Variable Scope yuansheng-9.2](doc/lua-variable-scope.md)
    * [Locations Configured by Subrequest Directives of Other Modules lance-2015.8.12](doc/locations-configured-by-subrequest-directives-of-other-modules.md)
    * [Cosockets Not Available Everywhere yuansheng-9.2](doc/cosockets-not-available-everywhere.md)
    * [特别转义序列 lance-2015.8.5](doc/special-escaping-sequences.md)
    * [Mixing with SSI Not Supported yuansheng-9.2](doc/mixing-with-ssi-not-supported.md)
    * [SPDY Mode Not Fully Supported yuansheng-9.2](doc/spdy-mode-not-fully-supported.md)
    * [Missing data on short circuited requests yuansheng-9.2](doc/missing-data-on-short-circuited-requests.md)
* [TODO yuansheng-9.3](doc/todo.md)
* [Changes yuansheng-9.3 moonbingbing(√)](doc/changes.md)
* [Test Suite yuansheng-9.3](doc/test-suite.md)
* [Copyright and License yuansheng-9.3](doc/copyright-and-license.md)
* [See Also yuansheng-9.3](doc/see-also.md)
* [Directives yuansheng-9.3](doc/directives.md)
* [Nginx API for Lua yuansheng-9.3](doc/nginx-api-for-lua.md)
* [Obsolete Sections yuansheng-9.3](doc/obsolete-sections.md)
    * [Special PCRE Sequences yuansheng-9.3](doc/special-pcre-sequences.md)

Directives
==========

* [lua_use_default_type hambut 2015.8.5](doc/lua-use-default-type.md)
* [lua_code_cache hambut 2015.8.5](doc/lua-code-cache.md)
* [lua_regex_cache_max_entries yuansheng-9.3](doc/lua_regex_cache_max_entries.md)
* [lua_regex_match_limit yuansheng-9.3](doc/lua_regex_match_limit.md)
* [lua_package_path yuansheng-9.4](doc/lua_package_path.md)
* [lua_package_cpath yuansheng-9.4](doc/lua_package_cpath.md)
* [init_by_lua yuansheng-9.4](doc/init_by_lua.md)
* [init_by_lua_file yuansheng-9.4](doc/init_by_lua_file.md)
* [init_worker_by_lua yuansheng-9.6](doc/init_worker_by_lua.md)
* [init_worker_by_lua_file yuansheng-9.6](doc/init_worker_by_lua_file.md)
* [set_by_lua yuansheng-9.6](doc/set_by_lua.md)
* [set_by_lua_file yuansheng-9.6](doc/set_by_lua_file.md)
* [content_by_lua dengshiyong 2015.8.12 moonbingbing(√)](doc/content_by_lua.md)
* [content_by_lua_file yuansheng-9.19](doc/content_by_lua_file.md)
* [rewrite_by_lua yuansheng-9.19](doc/rewrite_by_lua.md)
* [rewrite_by_lua_file yuansheng-9.19](doc/rewrite_by_lua_file.md)
* [access_by_lua yuansheng-9.27](doc/access_by_lua.md)
* [access_by_lua_file](#access_by_lua_file)
* [header_filter_by_lua liujinxuan 2015.9.1](doc/header_filter_by_lua.md)
* [header_filter_by_lua_file](#header_filter_by_lua_file)
* [body_filter_by_lua](#body_filter_by_lua)
* [body_filter_by_lua_file](#body_filter_by_lua_file)
* [log_by_lua](#log_by_lua)
* [log_by_lua_file](#log_by_lua_file)
* [lua_need_request_body](#lua_need_request_body)
* [lua_shared_dict lance-2015.8.20](doc/lua_shared_dict.md)
* [lua_socket_connect_timeout](#lua_socket_connect_timeout)
* [lua_socket_send_timeout](#lua_socket_send_timeout)
* [lua_socket_send_lowat](#lua_socket_send_lowat)
* [lua_socket_read_timeout](#lua_socket_read_timeout)
* [lua_socket_buffer_size](#lua_socket_buffer_size)
* [lua_socket_pool_size](#lua_socket_pool_size)
* [lua_socket_keepalive_timeout](#lua_socket_keepalive_timeout)
* [lua_socket_log_errors](#lua_socket_log_errors)
* [lua_ssl_ciphers](#lua_ssl_ciphers)
* [lua_ssl_crl](#lua_ssl_crl)
* [lua_ssl_protocols](#lua_ssl_protocols)
* [lua_ssl_trusted_certificate](#lua_ssl_trusted_certificate)
* [lua_ssl_verify_depth](#lua_ssl_verify_depth)
* [lua_http10_buffering](#lua_http10_buffering)
* [rewrite_by_lua_no_postpone](#rewrite_by_lua_no_postpone)
* [lua_transform_underscores_in_response_headers](#lua_transform_underscores_in_response_headers)
* [lua_check_client_abort](#lua_check_client_abort)
* [lua_max_pending_timers](#lua_max_pending_timers)
* [lua_max_running_timers](#lua_max_running_timers)

Nginx API for Lua
=================

* [Introduction lance-2015.9.6](doc/introduction.md)
* [ngx.arg lance-2015.8.19](doc/ngxarg.md)
* [ngx.var.VARIABLE lance-2015.8.19](doc/ngxvarvariable.md)
* [Core constants lance-2015.8.14 moonbingbing(√)](doc/core-constants.md)
* [HTTP method constants lance-2015.8.13](doc/http-method-constants.md)
* [HTTP status constants lance-2015.8.13](doc/http-status-constants.md)
* [Nginx log level constants lance-2015.8.13](doc/nginx-log-level-constants.md)
* [print lance-2015.8.14](doc/print.md)
* [ngx.ctx lance-2015.8.14](doc/ngxctx.md)
* [ngx.location.capture lance-2015.8.11](doc/ngxlocationcapture.md)
* [ngx.location.capture_multi lance-2015.8.11](doc/ngxlocationcapture_multi.md)
* [ngx.status lance-2015.8.18 yuansheng(√)](doc/ngxstatus.md)
* [ngx.header.HEADER lance-2015.9.6 yuansheng(√)](doc/ngxheaderheader.md)
* [ngx.resp.get_headers lance-2015.9.7 yuansheng(√)](doc/ngxrespget_headers.md)
* [ngx.req.start_time lance-2015.9.9 yuansheng(√)](doc/ngxreqstart_time.md)
* [ngx.req.http_version lance-2015.9.9 yuansheng(√)](doc/ngxreqhttp_version.md)
* [ngx.req.raw_header lance-2015.9.9 yuansheng(√)](doc/ngxreqraw_header.md)
* [ngx.req.get_method lance-2015.9.9 yuansheng(√)](doc/ngxreqget_method.md)
* [ngx.req.set_method lance-2015.9.9 yuansheng(√)](doc/ngxreqset_method.md)
* [ngx.req.set_uri lance-2015.9.9](doc/ngxreqset_uri.md)
* [ngx.req.set_uri_args lance-2015.9.10](doc/ngxreqset_uri_args.md)
* [ngx.req.get_uri_args lance-2015.9.10](doc/ngxreqget_uri_args.md)
* [ngx.req.get_post_args lance-2015.9.10](doc/ngxreqget_post_args.md)
* [ngx.req.get_headers lance-2015.9.11](doc/ngxreqget_headers.md)
* [ngx.req.set_header lance-2015.9.14](doc/ngxreqset_header.md)
* [ngx.req.clear_header lance-2015.9.14](doc/ngxreqclear_header.md)
* [ngx.req.read_body lance-2015.9.16](doc/ngxreqread_body.md)
* [ngx.req.discard_body lance-2015.9.24](doc/ngxreqdiscard_body.md)
* [ngx.req.get_body_data lance-2015.9.24](doc/ngxreqget_body_data.md)
* [ngx.req.get_body_file](#ngxreqget_body_file)
* [ngx.req.set_body_data](#ngxreqset_body_data)
* [ngx.req.set_body_file](#ngxreqset_body_file)
* [ngx.req.init_body](#ngxreqinit_body)
* [ngx.req.append_body](#ngxreqappend_body)
* [ngx.req.finish_body](#ngxreqfinish_body)
* [ngx.req.socket](#ngxreqsocket)
* [ngx.exec](#ngxexec)
* [ngx.redirect](#ngxredirect)
* [ngx.send_headers](#ngxsend_headers)
* [ngx.headers_sent](#ngxheaders_sent)
* [ngx.print lance-2015.8.7](doc/ngxprint.md)
* [ngx.say lance-2015.8.7](doc/ngxsay.md)
* [ngx.log lance-2015.8.13](doc/ngxlog.md)
* [ngx.flush lance-2015.8.13](doc/ngxflush.md)
* [ngx.exit lance-2015.8.13](doc/ngxexit.md)
* [ngx.eof lance-2015.8.18](doc/ngxeof.md)
* [ngx.sleep lance-2015.8.18](doc/ngxsleep.md)
* [ngx.escape_uri lance-2015.8.18](doc/ngxescape_uri.md)
* [ngx.unescape_uri lance-2015.8.18](doc/ngxunescape_uri.md)
* [ngx.encode_args lance-2015.8.18](doc/ngxencode_args.md)
* [ngx.decode_args lance-2015.8.18](doc/ngxdecode_args.md)
* [ngx.encode_base64 hambut-2015.9.9](doc/ngxencode_base64.md)
* [ngx.decode_base64 hambut-2015.9.9](doc/ngxdecode_base64.md)
* [ngx.crc32_short hambut-2015.9.9](doc/ngxcrc32_short.md)
* [ngx.crc32_long hambut-2015.9.9](doc/ngxcrc32_long.md)
* [ngx.hmac_sha1 hambut-2015.9.9](doc/ngxhmac_sha1.md)
* [ngx.md5 hambut-2015.9.9](doc/ngxmd5.md)
* [ngx.md5_bin hambut-2015.9.9](doc/ngxmd5_bin.md)
* [ngx.sha1_bin hambut-2015.9.9](doc/ngxsha1_bin.md)
* [ngx.quote_sql_str hambut-2015.9.9](doc/ngxquote_sql_str.md)
* [ngx.today bells-2015.8.8](doc/ngxtoday.md)
* [ngx.time bells-2015.8.22](doc/ngxtime.md)
* [ngx.now bells-2015.8.22](doc/ngxnow.md)
* [ngx.update_time bells-2015.8.16](doc/ngxupdate_time.md)
* [ngx.localtime bells-2015.8.22](doc/ngxlocaltime.md)
* [ngx.utctime bells-2015.8.22](doc/ngxutctime.md)
* [ngx.cookie_time](#ngxcookie_time)
* [ngx.http_time](#ngxhttp_time)
* [ngx.parse_http_time](#ngxparse_http_time)
* [ngx.is_subrequest](#ngxis_subrequest)
* [ngx.re.match lance-2015.8.6](doc/ngxrematch.md)
* [ngx.re.find lance-2015.8.6](doc/ngxrefind.md)
* [ngx.re.gmatch lance-2015.8.6](doc/ngxregmatch.md)
* [ngx.re.sub lance-2015.8.6](doc/ngxresub.md)
* [ngx.re.gsub lance-2015.8.6](doc/ngxregsub.md)
* [ngx.shared.DICT lance-2015.8.10](doc/ngxshareddict.md)
* [ngx.shared.DICT.get lance-2015.8.10](doc/ngxshareddictget.md)
* [ngx.shared.DICT.get_stale lance-2015.8.10](doc/ngxshareddictget_stale.md)
* [ngx.shared.DICT.set lance-2015.8.10](doc/ngxshareddictset.md)
* [ngx.shared.DICT.safe_set lance-2015.8.10](doc/ngxshareddictsafe_set.md)
* [ngx.shared.DICT.add lance-2015.8.10](doc/ngxshareddictadd.md)
* [ngx.shared.DICT.safe_add lance-2015.8.10](doc/ngxshareddictsafe_add.md)
* [ngx.shared.DICT.replace lance-2015.8.10](doc/ngxshareddictreplace.md)
* [ngx.shared.DICT.delete lance-2015.8.10](doc/ngxshareddictdelete.md)
* [ngx.shared.DICT.incr lance-2015.8.10](doc/ngxshareddictincr.md)
* [ngx.shared.DICT.flush_all lance-2015.8.10](doc/ngxshareddictflush_all.md)
* [ngx.shared.DICT.flush_expired lance-2015.8.10](doc/ngxshareddictflush_expired.md)
* [ngx.shared.DICT.get_keys lance-2015.8.10](doc/ngxshareddictget_keys.md)
* [ngx.socket.udp](#ngxsocketudp)
* [udpsock:setpeername](#udpsocksetpeername)
* [udpsock:send](#udpsocksend)
* [udpsock:receive](#udpsockreceive)
* [udpsock:close](#udpsockclose)
* [udpsock:settimeout](#udpsocksettimeout)
* [ngx.socket.tcp](#ngxsockettcp)
* [tcpsock:connect](#tcpsockconnect)
* [tcpsock:sslhandshake](#tcpsocksslhandshake)
* [tcpsock:send](#tcpsocksend)
* [tcpsock:receive](#tcpsockreceive)
* [tcpsock:receiveuntil](#tcpsockreceiveuntil)
* [tcpsock:close](#tcpsockclose)
* [tcpsock:settimeout](#tcpsocksettimeout)
* [tcpsock:setoption](#tcpsocksetoption)
* [tcpsock:setkeepalive](#tcpsocksetkeepalive)
* [tcpsock:getreusedtimes](#tcpsockgetreusedtimes)
* [ngx.socket.connect](#ngxsocketconnect)
* [ngx.get_phase](#ngxget_phase)
* [ngx.thread.spawn](#ngxthreadspawn)
* [ngx.thread.wait](#ngxthreadwait)
* [ngx.thread.kill](#ngxthreadkill)
* [ngx.on_abort](#ngxon_abort)
* [ngx.timer.at](#ngxtimerat)
* [ngx.config.debug](#ngxconfigdebug)
* [ngx.config.prefix](#ngxconfigprefix)
* [ngx.config.nginx_version](#ngxconfignginx_version)
* [ngx.config.nginx_configure](#ngxconfignginx_configure)
* [ngx.config.ngx_lua_version](#ngxconfigngx_lua_version)
* [ngx.worker.exiting](#ngxworkerexiting)
* [ngx.worker.pid](#ngxworkerpid)
* [ndk.set_var.DIRECTIVE](#ndkset_vardirective)
* [coroutine.create](#coroutinecreate)
* [coroutine.resume](#coroutineresume)
* [coroutine.yield](#coroutineyield)
* [coroutine.wrap](#coroutinewrap)
* [coroutine.running](#coroutinerunning)
* [coroutine.status](#coroutinestatus)
