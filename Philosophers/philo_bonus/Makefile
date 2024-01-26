# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: tlefebvr <marvin@42lausanne.ch>            +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/06/03 12:44:54 by tlefebvr          #+#    #+#              #
#    Updated: 2022/06/22 15:04:34 by tlefebvr         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

SRCS = main.c

SRCS += laucher.c init.c utils.c error_manager.c

OBJS = $(SRCS:.c=.o)

NAME = philo_bonus

CLANG = clang

FLAGS = -Wall -Wextra -Werror

INCLUDE = -lpthread

HEADER = philo.h


all : $(NAME)

$(NAME) : $(OBJS)
		$(CLANG) $(INCLUDE) $(FLAGS) -o $(NAME) $(OBJS)

clean: 
	rm -f $(OBJS)

fclean:
	rm -f $(OBJS)
	rm -f $(NAME) $(BONUS)

re: fclean all

%.o: %.c $(HEADER)
	$(CLANG) $(FLAGS) -c $< -o $(<:.c=.o)
