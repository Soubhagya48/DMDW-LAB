{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "name": "Untitled2.ipynb",
      "provenance": [],
      "authorship_tag": "ABX9TyM9KlUmHe3qG8UxYEA3zzcE",
      "include_colab_link": true
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "metadata": {
        "id": "view-in-github",
        "colab_type": "text"
      },
      "source": [
        "<a href=\"https://colab.research.google.com/github/Rachnagit-hub/DMDW-LAB/blob/main/18it019lab1.ipynb\" target=\"_parent\"><img src=\"https://colab.research.google.com/assets/colab-badge.svg\" alt=\"Open In Colab\"/></a>"
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "_a0BCNUE_WUS",
        "outputId": "e0429f24-9f5f-4ee2-b832-a8416e715121",
        "colab": {
          "base_uri": "https://localhost:8080/"
        }
      },
      "source": [
        "#python program for mean, median, and mode.\n",
        "\n",
        "from collections import Counter\n",
        "data=[float(i) for i in input().split()]\n",
        "n=len(data)\n",
        "mean=sum(data)/n\n",
        "print(\"Mean = \",mean)\n",
        "#calculation of median\n",
        "temp=data.copy()\n",
        "temp=sorted(temp)\n",
        "if n%2!=0:\n",
        "  print(\"Median = \",temp[n//2])\n",
        "else:\n",
        "  median=(temp[n//2]+temp[n//2+1])/2  \n",
        "  print(\"Median = \",median)\n",
        "#calculation of mode\n",
        "  cnt=Counter(data)\n",
        "  maxi=max(cnt.items(),key= lambda x:x[1])[1]\n",
        "  print(maxi)\n",
        "  mode=[]\n",
        "  for each in cnt.items():\n",
        "    if each[1]==maxi:\n",
        "      mode.append(each[0])\n",
        "      print(\"each[0] = \",each[0])\n",
        "    if len(mode)==n:\n",
        "      print(\"Not found\")\n",
        "    else:\n",
        "      print(\"Mode = \",mode)"
      ],
      "execution_count": 14,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "2 4 7 8 9 10\n",
            "Mean =  6.666666666666667\n",
            "Median =  8.5\n",
            "1\n",
            "each[0] =  2.0\n",
            "Mode =  [2.0]\n",
            "each[0] =  4.0\n",
            "Mode =  [2.0, 4.0]\n",
            "each[0] =  7.0\n",
            "Mode =  [2.0, 4.0, 7.0]\n",
            "each[0] =  8.0\n",
            "Mode =  [2.0, 4.0, 7.0, 8.0]\n",
            "each[0] =  9.0\n",
            "Mode =  [2.0, 4.0, 7.0, 8.0, 9.0]\n",
            "each[0] =  10.0\n",
            "Not found\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "SSkMqCBTGI5t",
        "outputId": "8c9a8203-2e33-48c8-a5eb-fd44c032e9e3",
        "colab": {
          "base_uri": "https://localhost:8080/"
        }
      },
      "source": [
        "# python program for standard deviation and variance.\n",
        "data=[float(i) for i in input().split()]\n",
        "n=len(data)\n",
        "mean=sum(data)/n\n",
        "sum1=0\n",
        "for e in data:\n",
        "  sum1+=(e-mean)**2\n",
        "variance=sum1/n\n",
        "print('Variance = ',variance)\n",
        "\n",
        "std=variance**(0.5)\n",
        "print(\"Standard Deviation = \",std)"
      ],
      "execution_count": 13,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "1 8 9 10 56\n",
            "Variance =  394.1600000000001\n",
            "Standard Deviation =  19.853463173965395\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "12Y1gFCBJJsY",
        "outputId": "454e833d-4535-4582-c117-e6431bf4707b",
        "colab": {
          "base_uri": "https://localhost:8080/"
        }
      },
      "source": [
        "#python programs.\n",
        "# 1.python program to check even or odd.\n",
        "num = int(input(\"Enter a number: \"))\n",
        "if (num % 2) == 0:\n",
        "   print(\"{0} is Even\".format(num))\n",
        "else:\n",
        "   print(\"{0} is Odd\".format(num))"
      ],
      "execution_count": 12,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Enter a number: 4\n",
            "4 is Even\n"
          ],
          "name": "stdout"
        }
      ]
    },
    {
      "cell_type": "code",
      "metadata": {
        "id": "ZuKSEpEzKw5r",
        "outputId": "a7975d51-67ef-445f-d81e-00d7e3d66777",
        "colab": {
          "base_uri": "https://localhost:8080/"
        }
      },
      "source": [
        "# 2. Greatest among three numbers.\n",
        "num1 = int(input(\"Enter ist number: \"))\n",
        "num2 = int(input(\"Enter 2nd number: \"))\n",
        "num3 = int(input(\"Enter 3rd number: \"))\n",
        "\n",
        "if (num1 >= num2) and (num1 >= num3):\n",
        "   largest = num1\n",
        "elif (num2 >= num1) and (num2 >= num3):\n",
        "   largest = num2\n",
        "else:\n",
        "   largest = num3\n",
        "\n",
        "print(\"The largest number is\", largest)"
      ],
      "execution_count": 11,
      "outputs": [
        {
          "output_type": "stream",
          "text": [
            "Enter ist number: 5\n",
            "Enter 2nd number: 7\n",
            "Enter 3rd number: 8\n",
            "The largest number is 8\n"
          ],
          "name": "stdout"
        }
      ]
    }
  ]
} 
