CC = gcc

CFLAGS = -Imlx-linux -c -Wall -Wextra -Werror
LFLAGS = -Lmlx-linux -L/usr/lib -lXext -lX11 -lm -lbsd

NAME = fract-ol
SRC = ft_cplx_ops.c ft_cplx_extra.c fractol_main.c fractol_utils_1.c fractol_utils_2.c fractol_utils_3.c fractol_parsing.c
OBJ = $(SRC:%.c=%.o)
LIBOBJ = \
		mlx-linux/obj/mlx_clear_window.o \
		mlx-linux/obj/mlx_destroy_display.o \
		mlx-linux/obj/mlx_destroy_image.o \
		mlx-linux/obj/mlx_destroy_window.o \
		mlx-linux/obj/mlx_expose_hook.o \
		mlx-linux/obj/mlx_flush_event.o \
		mlx-linux/obj/mlx_get_color_value.o \
		mlx-linux/obj/mlx_get_data_addr.o \
		mlx-linux/obj/mlx_hook.o \
		mlx-linux/obj/mlx_init.o \
		mlx-linux/obj/mlx_int_anti_resize_win.o \
		mlx-linux/obj/mlx_int_do_nothing.o \
		mlx-linux/obj/mlx_int_get_visual.o \
		mlx-linux/obj/mlx_int_param_event.o \
		mlx-linux/obj/mlx_int_set_win_event_mask.o \
		mlx-linux/obj/mlx_int_str_to_wordtab.o \
		mlx-linux/obj/mlx_int_wait_first_expose.o \
		mlx-linux/obj/mlx_key_hook.o \
		mlx-linux/obj/mlx_loop_hook.o \
		mlx-linux/obj/mlx_loop.o \
		mlx-linux/obj/mlx_mouse_hook.o \
		mlx-linux/obj/mlx_mouse.o \
		mlx-linux/obj/mlx_new_image.o \
		mlx-linux/obj/mlx_new_window.o \
		mlx-linux/obj/mlx_pixel_put.o \
		mlx-linux/obj/mlx_put_image_to_window.o \
		mlx-linux/obj/mlx_rgb.o \
		mlx-linux/obj/mlx_screen_size.o \
		mlx-linux/obj/mlx_set_font.o \
		mlx-linux/obj/mlx_string_put.o \
		mlx-linux/obj/mlx_xpm.o \


all: $(NAME)

$(NAME): $(OBJ)
	$(CC) -o $(NAME) $(OBJ) $(LIBOBJ) $(LFLAGS)

%.o: %.c
	$(CC) $(CFLAGS) $(SRC)

clean:
	rm -f $(OBJ)

fclean: clean
	rm -f $(NAME)

re: fclean all