# logger
Boilerplate config for logging config


* The logger is being defined per module with Null handler.

# Init logger in the top level script

# Set up logger for the script
import logging.config
logger = logging.getLogger(__name__)
with open('logger/dev.json', 'rt') as f:
    config = json.load(f)
logging.config.dictConfig(config)
# --- End setup logger ---
