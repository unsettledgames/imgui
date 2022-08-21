# Set where the ImGui files are stored
set(IMGUI_PATH  .)
    

add_library("imgui" STATIC 
	"imconfig.h"
	"imgui.h"
	"imgui.cpp"
	"imgui_draw.cpp"
	"imgui_internal.h"
	"imgui_tables.cpp"
	"imgui_widgets.cpp"
	"imstb_rectpack.h"
	"imstb_textedit.h"
	"imstb_truetype.h"
	"imgui_demo.cpp"
)
target_include_directories("imgui" 
	PUBLIC ${IMGUI_PATH}
	PUBLIC ${IMGUI_PATH}/backends
	PRIVATE ${IMGUI_PATH}/examples
)
