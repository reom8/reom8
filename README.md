[root@localhost scrapydweb]# scrapydweb
[2022-09-01 10:48:12,569] INFO     in apscheduler.scheduler: Scheduler started
Traceback (most recent call last):
  File "/usr/local/python38/bin/scrapydweb", line 5, in <module>
    from scrapydweb.run import main
  File "/usr/local/python38/lib/python3.8/site-packages/scrapydweb/run.py", line 15, in <module>
    from scrapydweb.utils.check_app_config import check_app_config
  File "/usr/local/python38/lib/python3.8/site-packages/scrapydweb/utils/check_app_config.py", line 16, in <module>
    from .sub_process import init_logparser, init_poll
  File "/usr/local/python38/lib/python3.8/site-packages/scrapydweb/utils/sub_process.py", line 3, in <module>
    from ctypes import cdll
  File "/usr/local/python38/lib/python3.8/ctypes/__init__.py", line 7, in <module>
    from _ctypes import Union, Structure, Array
ModuleNotFoundError: No module named '_ctypes'
[2022-09-01 10:48:12,577] DEBUG    in apscheduler: Scheduled tasks: []
[2022-09-01 10:48:12,577] WARNING  in apscheduler: Shutting down the scheduler for timer tasks gracefully, wait until all currently executing tasks are finished
Error in atexit._run_exitfuncs:
Traceback (most recent call last):
  File "/usr/local/python38/lib/python3.8/site-packages/scrapydweb/utils/scheduler.py", line 111, in <lambda>
    atexit.register(lambda: shutdown_scheduler())
  File "/usr/local/python38/lib/python3.8/site-packages/scrapydweb/utils/scheduler.py", line 98, in shutdown_scheduler
    handle_metadata().get('main_pid'))
  File "/usr/local/python38/lib/python3.8/site-packages/scrapydweb/common.py", line 84, in handle_metadata
    with db.app.app_context():
AttributeError: 'NoneType' object has no attribute 'app_context'
