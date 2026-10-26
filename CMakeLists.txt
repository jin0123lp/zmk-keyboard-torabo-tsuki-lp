if(CONFIG_SHIELD_TORABO_TSUKI_LP_LEFT OR CONFIG_SHIELD_TORABO_TSUKI_LP_RIGHT)
  zephyr_library()
  zephyr_include_directories(${APPLICATION_SOURCE_DIR}/include)
  # 実験: 左右間の接続パラメータを切り替える省電力処理(src/board.c)を無効化
  zephyr_library_sources(src/mini_trackpad_init_reg.c)
endif()
