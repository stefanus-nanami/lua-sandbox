CD = cd
CP_DIR = cp -r
MAKE = make
RM_DIR = rm -rf
BUILD_PATH = $(shell pwd)/..

.PHONY: clean lua lua-clean lib luabridge lrdb picojson asio

clean: lua-clean
	$(RM_DIR) $(BUILD_PATH)/bin
	$(RM_DIR) $(BUILD_PATH)/include
	$(RM_DIR) $(BUILD_PATH)/lib
	$(RM_DIR) $(BUILD_PATH)/man
	$(RM_DIR) $(BUILD_PATH)/share

lua-clean:
	$(CD) lua && $(MAKE) clean

lua:
	$(CD) lua && $(MAKE) all install INSTALL_TOP=$(BUILD_PATH) CC="clang -std=gnu99"

luabridge:
	$(CP_DIR) LuaBridge3/Distribution/LuaBridge $(BUILD_PATH)/include/LuaBridge

lrdb:
	$(CP_DIR) LRDB/include/LRDB $(BUILD_PATH)/include/LRDB

picojson:
	$(CP_DIR) picojson/picojson.h $(BUILD_PATH)/include

asio:
	$(CP_DIR) asio/asio/include $(BUILD_PATH)/include/asio

lib: lua luabridge lrdb picojson asio

