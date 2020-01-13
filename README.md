# Spring Validation Annotation

### javax.validation
- [@AssertFalse](#assertfalse)
- [@AssertTrue](#asserttrue)
- [@DecimalMax](#decimalmaxvalue-inclusive)
- [@DecimalMin](#decimalminvalue-inclusive)
- [@Digits](#digitsinteger-fraction)
- [@Email](#emailregexp-flags)
- [@Future](#future)
- [@FutureOrPresent](#futureorpresent)
- [@Max](#maxvalue)
- [@Min](#minvalue)
- [@Negative](#negative)
- [@NegativeOrZero](#negativeorzero)
- [@NotBlank](#notblank)
- [@NotEmpty](#notempty)
- [@NotNull](#notnull)
- [@Null](#null)
- [@Past](#past)
- [@PastOrPresent](#pastorpresent)
- [@Pattern](#patternregexp-flags)
- [@Positive](#positive)
- [@Size](#sizemin-max)

#### @AssertFalse
```
주석이 달린 요소는 거짓이어야 합니다.
지원되는 타입은 boolean과 Boolean 입니다.
null 요소는 유효한 것으로 간주됩니다.
```
#### @AssertTrue
```
주석이 달린 요소는 참이어야 합니다.
지원되는 타입은 boolean과 Boolean 입니다.
null 요소는 유효한 것으로 간주됩니다.
```
#### @DecimalMax(value*=, inclusive=)
```
주석이 달린 요소는 value보다 작거나 같아야합니다.
지원되는 타입은 BigDecimal, BigInteger, CharSequence, 그리고 byte, short, int, long 및 각각의 래퍼입니다.
반올림 오류로 인해 double과 float는 지원되지 않습니다. (일부 제공 업체는 대략적인 지원을 제공할 수 있습니다.)
null 요소는 유효한 것으로 간주됩니다.
inclusive가 true인 경우 주석이 달린 요소는 value보다 크거나 같아야 하고, false인 경우 value보다 커야 합니다.
```

#### @DecimalMin(value*=, inclusive=)
```
주석이 달린 요소는 value보다 크거나 같아야합니다.
지원되는 타입은 BigDecimal, BigInteger, CharSequence, 그리고 byte, short, int, long 및 각각의 래퍼입니다.
반올림 오류로 인해 double과 float는 지원되지 않습니다. (일부 제공 업체는 대략적인 지원을 제공할 수 있습니다.)
null 요소는 유효한 것으로 간주됩니다.
추가적으로 inclusive가 true인 경우 주석이 달린 요소는 value보다 크거나 같아야 하고, false인 경우 value보다 커야 합니다.
```

#### @Digits(integer*=, fraction*=)
```
주석이 달린 요소는 허용되는 범위 내의 숫자여야 합니다.
지원되는 타입은 BigDecimal, BigInteger, CharSequence, 그리고 byte, short, int, long 및 각각의 래퍼입니다.
null 요소는 유효한 것으로 간주됩니다.
integer는 허용되는 최대 정수 자릿수, fraction은 허용되는 최대 소수 자릿수입니다.
```

#### @Email(regexp=, flags=)
```
주석이 달린 문자열은 올바른 형식의 이메일 주소여야 합니다. 
유효한 이메일 주소에 대한 정확한 의미는 빈 검증 제공자에게 달려있습니다.
CharSequence 타입을 허용합니다.
```

#### @Future
```
주석이 달린 요소는 미래의 순간, 날짜 또는 시간이어야 합니다.
현재는 Validator 또는 ValidatorFactory에 첨부된 ClockProvider에 의해 결정됩니다.
지원되는 타입은 Date, Calendar, Instant, LocalDate, LocalDateTime, LocalTime, MonthDay, OffsetDateTime, OffsetTime, Year, YearMonth, ZonedDateTime, HijrahDate, JapaneseDate, MinguoDate, ThaiBuddhistDate입니다.
null 요소는 유효한 것으로 간주됩니다.
```

#### @FutureOrPresent
```
주석이 달린 요소는 현재 또는 미래의 순간, 날짜 또는 시간이어야 합니다.
현재는 Validator 또는 ValidatorFactory에 첨부된 ClockProvider에 의해 결정됩니다.
여기서 현재의 개념은 제약 조건에 따라 상대적으로 정의됩니다.
예를 들어 제약 조건이 Year에 있는 경우 현제는 현재 연도 전체를 의미합니다.
지원되는 타입은 Date, Calendar, Instant, LocalDate, LocalDateTime, LocalTime, MonthDay, OffsetDateTime, OffsetTime, Year, YearMonth, ZonedDateTime, HijrahDate, JapaneseDate, MinguoDate, ThaiBuddhistDate입니다.
null 요소는 유효한 것으로 간주됩니다.
```

#### @Max(value*=)
```
주석이 달린 요소는 value보다 작거나 같아야 합니다.
지원되는 타입은 BigDecimal, BigInteger, 그리고 byte, short, int, long 및 각각의 래퍼입니다. 
반올림 오류로 인해 double과 float는 지원되지 않습니다. (일부 제공 업체는 대략적인 지원을 제공할 수 있습니다.)
null 요소는 유효한 것으로 간주됩니다.
```

#### @Min(value*=)
```
주석이 달린 요소는 value보다 크거나 같아야 합니다.
지원되는 타입은 BigDecimal, BigInteger, 그리고 byte, short, int, long 및 각각의 래퍼입니다. 
반올림 오류로 인해 double과 float는 지원되지 않습니다. (일부 제공 업체는 대략적인 지원을 제공할 수 있습니다.)
null 요소는 유효한 것으로 간주됩니다.
```

#### @Negative
```
주석이 달린 요소는 음수여야 합니다. (0은 잘못된 값입니다.)
지원되는 타입은 BigDecimal, BigInteger, 그리고 byte, short, int, long, float, double 및 각각의 래퍼입니다.
null 요소는 유효한 것으로 간주됩니다.
```

#### @NegativeOrZero 
```
주석이 달린 요소는 음수 또는 0 이어야 합니다.
지원되는 타입은 BigDecimal, BigInteger, 그리고 byte, short, int, long, float, double 및 각각의 래퍼입니다.
null 요소는 유효한 것으로 간주됩니다.
```

#### @NotBlank
```
주석이 달린 요소는 null이 아니어야 하며, 하나 이상의 공백이 아닌 문자를 포함해야 합니다.
CharSequence 타입을 허용합니다.
```

#### @NotEmpty
```
주석이 달린 요소는 null이거나 비어있으면 안됩니다.
지원되는 타입은 CharSequence, Collection, Map, 배열입니다.
각각의 길이나 크기가 평가됩니다.
```

#### @NotNull
```
주석이 달린 요소는 null이 아니어야 합니다.
모든 타입을 허용합니다.
```

#### @Null
```
주석이 달린 요소는 null 이어야 합니다.
모든 타입을 허용합니다.
```

#### @Past
```
주석이 달린 요소는 과거의 순간, 날짜 또는 시간이어야 합니다.
현재는 Validator 또는 ValidatorFactory에 첨부된 ClockProvider에 의해 결정됩니다.
지원되는 타입은 Date, Calendar, Instant, LocalDate, LocalDateTime, LocalTime, MonthDay, OffsetDateTime, OffsetTime, Year, YearMonth, ZonedDateTime, HijrahDate, JapaneseDate, MinguoDate, ThaiBuddhistDate입니다.
null 요소는 유효한 것으로 간주됩니다.
```

#### @PastOrPresent
```
주석이 달린 요소는 현재 또는 과거의 순간, 날짜 또는 시간이어야 합니다.
현재는 Validator 또는 ValidatorFactory에 첨부된 ClockProvider에 의해 결정됩니다.
여기서 현재의 개념은 제약 조건에 따라 상대적으로 정의됩니다.
예를 들어 제약 조건이 Year에 있는 경우 현제는 현재 연도 전체를 의미합니다.
지원되는 타입은 Date, Calendar, Instant, LocalDate, LocalDateTime, LocalTime, MonthDay, OffsetDateTime, OffsetTime, Year, YearMonth, ZonedDateTime, HijrahDate, JapaneseDate, MinguoDate, ThaiBuddhistDate입니다.
null 요소는 유효한 것으로 간주됩니다.
```

#### @Pattern(regexp*=, flags=)
```
주석이 달린 CharSequence는 지정된 정규식과 일치해야 합니다.
정규식은 Java 정규식 규칙을 따릅니다.
null 요소는 유효한 것으로 간주됩니다.

가능한 Regex flags
UNIX_LINES: 유닉스 라인 모드 활성화
CASE_INSENSITIVE: 대소문자 구분없이 일치 가능
COMMENTS: 패턴으로 공백 및 주석 허용
MULTILINE: 멀티 라인 모드 활성화
DOTALL: dotall 모드 활성화('\n' 문자 포함 매칭)
UNICODE_CASE: 유니코드 인식 케이스 폴딩 지원
CANON_EQ: 규범적 동등성 활성화
```

#### @Positive
```
주석이 달린 요소는 양수여야 합니다. (0은 잘못된 값입니다.)
지원되는 타입은 BigDecimal, BigInteger, 그리고 byte, short, int, long, float, double 및 각각의 래퍼입니다.
null 요소는 유효한 것으로 간주됩니다.
```

#### @PositiveOrZero
```
주석이 달린 요소는 양수 또는 0 이어야 합니다.
지원되는 타입은 BigDecimal, BigInteger, 그리고 byte, short, int, long, float, double 및 각각의 래퍼입니다.
null 요소는 유효한 것으로 간주됩니다.
```

#### @Size(min=, max=)
```
int min(default: 0), int max(default: 2147483647)
주석이 달린 요소의 크기는 지정된 경계를 포함한 사이에 있어야 합니다.
지원되는 타입은 CharSequence, Collection, Map, 배열입니다.
null 요소는 유효한 것으로 간주됩니다.
요소의 크기는 min보다 크거나 같아야 하고, max보다 작거나 같아야 합니다.
```
