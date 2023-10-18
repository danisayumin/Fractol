# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: danielasayuminitta <danielasayuminitta@    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/08/17 22:10:43 by dsayumi-          #+#    #+#              #
#    Updated: 2023/10/18 19:36:13 by danielasayu      ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME		= libftprintf.a
CC			= cc
CFLAGS		= -Wall -Wextra -Werror
INCS		= ft_fractol.h
SRCS		= ft_fractol.c \

OBJS		= $(SRCS:.c=.o)

UNAME	:= $(shell uname)
ifeq ($(UNAME), Darwin) #MACOS
	CFLAGS = libmlx42.a -Iinclude -lglfw -L"/opt/homebrew/Cellar/glfw/3.3.8/lib/"
all: 		$(NAME)

$(NAME):	$(OBJS) $(INCS)
	ar -rcs	$(NAME) $(OBJS)

.c.o: 		
	$(CC) $(CFLAGS) -c $< -o $(<:.c=.o)
=
bonus: all

clean:
	rm -f $(OBJS)

fclean: clean
	rm -f $(NAME)

re: fclean all

.PHONY: all clean fclean re