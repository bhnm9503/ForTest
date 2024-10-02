# you

cp / /root/nulink


chmod -R 77 /root/nulink

pip install virtualenv

virtualenv /root/nulink-venv

source /root/nulink-venv/bin/activate

wget https://filetransfer.nulink.org/release/nulink-0.2.0-py3-none-any.whl

pip install nulink-0.0-py3-none-any.whl

pip install --upgrade pip

source /root/nulink-venv/bin/activate

python -c "import nulink"

nulink --help

export NULINK_KEYSTORE_PASSWORD=xxxxxxxxxxxx

Ø¨Ù‡ Ø¬Ø§ÛŒ Ø§ÛŒÚ©Ø³ Ù‡Ø§ Ø§ÙˆÙ† Ù¾Ø³ÙˆØ±Ø¯ Ú©Ù‡ Ø¨Ø§Ù„Ø§ØªØ± ÙˆØ§Ø±Ø¯ Ú©Ø±Ø¯ÛŒØ¯ Ùˆ Ú¯ÙØªÙ… Ø¯Ø± Ø§Ø¯Ø§Ù…Ù‡ Ù„Ø§Ø²Ù…ÙˆÙ† Ù…ÛŒØ´Ù‡ Ø±Ùˆ ÙˆØ§Ø±Ø¯ Ú©Ù†ÛŒØ¯

export NULINK_OPERATOR_ETH_PASSWORD=xxxxxxxxxx

Ø¯Ø± Ø§ÛŒÙ†Ø¬Ø§ Ù‡Ù… Ø¨Ù‡ Ø¬Ø§ÛŒ Ø§ÛŒÚ©Ø³ Ù‡Ø§ Ø§ÙˆÙ† Ù¾Ø³ÙˆØ±Ø¯ÛŒ Ú©Ù‡ Ø¨Ø§Ù„Ø§ØªØ± Ø¯Ø§Ø¯ÛŒØ¯ Ø±Ùˆ Ø¯ÙˆØ¨Ø§Ø±Ù‡ ÙˆØ§Ø±Ø¯ Ú©Ù†ÛŒØ¯

docker run -it --rm \
-p 9151:9151 \
-v /root/nulink:/code \
-v /root/nulink:/home/circleci/.local/share/nulink \
-e NULINK_KEYSTORE_PASSWORD \
nulink/nulink nulink ursula init \
--signer keystore:///code/xxxxxxxxxxxxxxxxxxxxxxx \
--eth-provider https://data-seed-prebsc-2-s2.binance.org:8545/ \
--network horus \
--payment-provider https://data-seed-prebsc-2-s2.binance.org:8545/ \
--payment-network bsc_testnet \
--operator-address yyyyyyyyyyyyyyy \
--max-gas-price 100
