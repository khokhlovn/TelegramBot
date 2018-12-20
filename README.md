# TelegramBot
USE [master]
GO
/****** Object:  Database [TelegramBot]    Script Date: 19.12.2018 18:05:58 ******/
CREATE DATABASE [TelegramBot]
 CONTAINMENT = NONE
 ON  PRIMARY 
( NAME = N'TelegramBot', FILENAME = N'C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\TelegramBot.mdf' , SIZE = 8192KB , MAXSIZE = UNLIMITED, FILEGROWTH = 65536KB )
 LOG ON 
( NAME = N'TelegramBot_log', FILENAME = N'C:\Program Files\Microsoft SQL Server\MSSQL14.MSSQLSERVER\MSSQL\DATA\TelegramBot_log.ldf' , SIZE = 8192KB , MAXSIZE = 2048GB , FILEGROWTH = 65536KB )
GO
ALTER DATABASE [TelegramBot] SET COMPATIBILITY_LEVEL = 140
GO
IF (1 = FULLTEXTSERVICEPROPERTY('IsFullTextInstalled'))
begin
EXEC [TelegramBot].[dbo].[sp_fulltext_database] @action = 'enable'
end
GO
ALTER DATABASE [TelegramBot] SET ANSI_NULL_DEFAULT OFF 
GO
ALTER DATABASE [TelegramBot] SET ANSI_NULLS OFF 
GO
ALTER DATABASE [TelegramBot] SET ANSI_PADDING OFF 
GO
ALTER DATABASE [TelegramBot] SET ANSI_WARNINGS OFF 
GO
ALTER DATABASE [TelegramBot] SET ARITHABORT OFF 
GO
ALTER DATABASE [TelegramBot] SET AUTO_CLOSE OFF 
GO
ALTER DATABASE [TelegramBot] SET AUTO_SHRINK OFF 
GO
ALTER DATABASE [TelegramBot] SET AUTO_UPDATE_STATISTICS ON 
GO
ALTER DATABASE [TelegramBot] SET CURSOR_CLOSE_ON_COMMIT OFF 
GO
ALTER DATABASE [TelegramBot] SET CURSOR_DEFAULT  GLOBAL 
GO
ALTER DATABASE [TelegramBot] SET CONCAT_NULL_YIELDS_NULL OFF 
GO
ALTER DATABASE [TelegramBot] SET NUMERIC_ROUNDABORT OFF 
GO
ALTER DATABASE [TelegramBot] SET QUOTED_IDENTIFIER OFF 
GO
ALTER DATABASE [TelegramBot] SET RECURSIVE_TRIGGERS OFF 
GO
ALTER DATABASE [TelegramBot] SET  DISABLE_BROKER 
GO
ALTER DATABASE [TelegramBot] SET AUTO_UPDATE_STATISTICS_ASYNC OFF 
GO
ALTER DATABASE [TelegramBot] SET DATE_CORRELATION_OPTIMIZATION OFF 
GO
ALTER DATABASE [TelegramBot] SET TRUSTWORTHY OFF 
GO
ALTER DATABASE [TelegramBot] SET ALLOW_SNAPSHOT_ISOLATION OFF 
GO
ALTER DATABASE [TelegramBot] SET PARAMETERIZATION SIMPLE 
GO
ALTER DATABASE [TelegramBot] SET READ_COMMITTED_SNAPSHOT OFF 
GO
ALTER DATABASE [TelegramBot] SET HONOR_BROKER_PRIORITY OFF 
GO
ALTER DATABASE [TelegramBot] SET RECOVERY FULL 
GO
ALTER DATABASE [TelegramBot] SET  MULTI_USER 
GO
ALTER DATABASE [TelegramBot] SET PAGE_VERIFY CHECKSUM  
GO
ALTER DATABASE [TelegramBot] SET DB_CHAINING OFF 
GO
ALTER DATABASE [TelegramBot] SET FILESTREAM( NON_TRANSACTED_ACCESS = OFF ) 
GO
ALTER DATABASE [TelegramBot] SET TARGET_RECOVERY_TIME = 60 SECONDS 
GO
ALTER DATABASE [TelegramBot] SET DELAYED_DURABILITY = DISABLED 
GO
EXEC sys.sp_db_vardecimal_storage_format N'TelegramBot', N'ON'
GO
ALTER DATABASE [TelegramBot] SET QUERY_STORE = OFF
GO
USE [TelegramBot]
GO
ALTER DATABASE SCOPED CONFIGURATION SET IDENTITY_CACHE = ON;
GO
ALTER DATABASE SCOPED CONFIGURATION SET LEGACY_CARDINALITY_ESTIMATION = OFF;
GO
ALTER DATABASE SCOPED CONFIGURATION FOR SECONDARY SET LEGACY_CARDINALITY_ESTIMATION = PRIMARY;
GO
ALTER DATABASE SCOPED CONFIGURATION SET MAXDOP = 0;
GO
ALTER DATABASE SCOPED CONFIGURATION FOR SECONDARY SET MAXDOP = PRIMARY;
GO
ALTER DATABASE SCOPED CONFIGURATION SET PARAMETER_SNIFFING = ON;
GO
ALTER DATABASE SCOPED CONFIGURATION FOR SECONDARY SET PARAMETER_SNIFFING = PRIMARY;
GO
ALTER DATABASE SCOPED CONFIGURATION SET QUERY_OPTIMIZER_HOTFIXES = OFF;
GO
ALTER DATABASE SCOPED CONFIGURATION FOR SECONDARY SET QUERY_OPTIMIZER_HOTFIXES = PRIMARY;
GO
USE [TelegramBot]
GO
/****** Object:  Table [dbo].[Fridge]    Script Date: 19.12.2018 18:05:59 ******/
SET ANSI_NULLS ON
GO
SET QUOTED_IDENTIFIER ON
GO
CREATE TABLE [dbo].[Fridge](
	[Id_fridge] [int] NOT NULL,
	[products] [varchar](max) NULL
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
GO
USE [master]
GO
ALTER DATABASE [TelegramBot] SET  READ_WRITE 
GO
CREATE TABLE [dbo].[Recipe](
	[Id_recipe] [int] NOT NULL,
	[Name] [varchar](30) NOT NULL,
	[Fridge_id] [int] NOT NULL,
	[Ingredients] [varchar](max) NOT NULL,
	[Recipe][varchar](max),
) ON [PRIMARY] TEXTIMAGE_ON [PRIMARY]
GO
USE [master]
GO
ALTER DATABASE [TelegramBot] SET  READ_WRITE 
GO
