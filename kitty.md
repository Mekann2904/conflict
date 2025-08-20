```
# =================================================================
# Kitty Terminal Configuration
# =================================================================

# ----------------------------------
# 1. 全般設定 (General)
# ----------------------------------

# 他のプログラムからのkittyのリモートコントロールをソケット経由でのみ許可
allow_remote_control socket-only

# OSのウィンドウを閉じる操作時に確認ダイアログを表示しない (0 = しない)
confirm_os_window_close 0

# アクティブでないウィンドウの背景を半透明にする
dynamic_background_opacity yes

# kitty独自のショートカットキーの修飾キー（モディファイア）
kitty_mod cmd+shift

# 使用可能なウィンドウレイアウトを `splits` (分割) に限定
enabled_layouts splits

# kitty起動時に読み込むセッションファイル
# startup_session ~/.config/kitty/startup-session.conf


# ----------------------------------
# 2. 外観 (Appearance)
# ----------------------------------

### テーマ: Tokyo Night ###
## name: Tokyo Night
## license: MIT
## author: Folke Lemaitre
## upstream: https://github.com/folke/tokyonight.nvim/raw/main/extras/kitty/tokyonight_night.conf
background #1a1b26
foreground #c0caf5
selection_background #283457
selection_foreground #c0caf5
url_color #73daca
cursor #c0caf5
cursor_text_color #1a1b26

### タブバー (Tabs) ###
active_tab_background #7aa2f7
active_tab_foreground #16161e
inactive_tab_background #292e42
inactive_tab_foreground #545c7e
#tab_bar_background #15161e

### ウィンドウ (Windows) ###
active_border_color #7aa2f7
inactive_border_color #292e42

### 背景画像 (Background Image) ###
# background_image /Users/mekann/kitty.png
# background_tint 0.9
# background_image_layout  cscaled

### カラーパレット (Color Palette) ###
# normal
color0 #15161e
color1 #f7768e
color2 #9ece6a
color3 #e0af68
color4 #7aa2f7
color5 #bb9af7
color6 #7dcfff
color7 #a9b1d6

# bright
color8  #414868
color9  #ff899d
color10 #9fe044
color11 #faba4a
color12 #8db0ff
color13 #c7a9ff
color14 #a4daff
color15 #c0caf5

# extended colors
color16 #ff9e64
color17 #db4b4b


# ----------------------------------
# 3. キーマッピング (Key Mappings)
# ----------------------------------

# 新しいウィンドウを水平分割で開く
map kitty_mod+enter launch --location=hsplit --cwd=current zsh

# ウィンドウのレイアウト変更
map cmd+space next_layout

# 次のタブへ移動
map cmd+shift+n next_tab

# 前のタブへ移動
map cmd+shift+p previous_tab

# Vimライクなキーバインドでウィンドウ間を移動
map cmd+h neighboring_window left
map cmd+j neighboring_window down
map cmd+k neighboring_window up
map cmd+l neighboring_window right

# Vimライクなキーバインドでウィンドウサイズを変更
map kitty_mod+shift+h resize_window narrower
map kitty_mod+shift+j resize_window taller
map kitty_mod+shift+k resize_window shorter
map kitty_mod+shift+l resize_window wider

# ----------------------------------
# 4. その他 (Miscellaneous)
# ----------------------------------

# クリックしたURLをOSのデフォルトブラウザで開く
open_url_with default

# Kittyにシェルからのタブタイトル制御を許可
tab_title_template "{title}"
window_title_format "{title}"

# Vim用モデルライン (このファイルがkitty設定ファイルであることを示す)
# vim:ft=kitty

```
