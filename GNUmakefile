CC = gcc

CFLAGS = -Imlx -c -Wall -Wextra -Werror
LFLAGS = -Lmlx -L/usr/lib -lXext -lX11 -lm -lbsd

NAME = fract-ol
SRC = ft_cplx_ops.c ft_cplx_extra.c fractol_main.c fractol_utils_1.c fractol_utils_2.c fractol_utils_3.c fractol_parsing.c
OBJ = $(SRC:%.c=%.o)
LIBOBJ = \
		mlx/obj/mlx_clear_window.o \
		mlx/obj/mlx_destroy_display.o \
		mlx/obj/mlx_destroy_image.o \
		mlx/obj/mlx_destroy_window.o \
		mlx/obj/mlx_expose_hook.o \
		mlx/obj/mlx_flush_event.o \
		mlx/obj/mlx_get_color_value.o \
		mlx/obj/mlx_get_data_addr.o \
		mlx/obj/mlx_hook.o mlx/obj/mlx_init.o \
		mlx/obj/mlx_int_anti_resize_win.o \
		mlx/obj/mlx_int_do_nothing.o \
		mlx/obj/mlx_int_get_visual.o \
		mlx/obj/mlx_int_param_event.o \
		mlx/obj/mlx_int_set_win_event_mask.o \
		mlx/obj/mlx_int_str_to_wordtab.o \
		mlx/obj/mlx_int_wait_first_expose.o \
		mlx/obj/mlx_key_hook.o \
		mlx/obj/mlx_loop_hook.o \
		mlx/obj/mlx_loop.o mlx/obj/mlx_mouse_hook.o \
		mlx/obj/mlx_mouse.o mlx/obj/mlx_new_image.o \
		mlx/obj/mlx_new_window.o \
		mlx/obj/mlx_pixel_put.o \
		mlx/obj/mlx_put_image_to_window.o mlx/obj/mlx_rgb.o \
		mlx/obj/mlx_screen_size.o \
		mlx/obj/mlx_set_font.o \
		mlx/obj/mlx_string_put.o \
		mlx/obj/mlx_xpm.o \


all: $(NAME)

$(NAME): $(OBJ)
	$(CC) -o $(NAME) $(OBJ) $(LIBOBJ) $(LFLAGS)

%.o: %.c
	$(CC) $(CFLAGS) $(SRC)

clean:
	rm -f $(SRC:%.c=%.o)

fclean: clean
	rm -f $(NAME)

re: fclean all