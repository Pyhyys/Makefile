# 定義編譯器
CXX = g++
# 定義編譯選項
CXXFLAGS = -Wall -g
# 定義目標執行檔
TARGET = my_program

# 定義依賴關係與編譯規則
all: $(TARGET)

# 分隔一定要用 "TAB" 不要用 "空格"
$(TARGET): main.o utils.o
	$(CXX) $(CXXFLAGS) -o $(TARGET) main.o utils.o

main.o: main.cpp utils.h
	$(CXX) $(CXXFLAGS) -c main.cpp

utils.o: utils.cpp utils.h
	$(CXX) $(CXXFLAGS) -c utils.cpp

# 清理編譯生成的檔案
clean:
	rm -f $(TARGET) *.o

# 運行程式
run: $(TARGET)
	./$(TARGET)
