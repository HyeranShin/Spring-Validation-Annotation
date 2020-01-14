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

### org.hibernate.validation
- [@CNPJ](#cnpj)
- [@CPF](#cpf)
- [@TituloEleitoral](#tituloeleitoral)
- [@NIP](#nip)
- [@PESEL](#pesel)
- [@REGON](#regon)
- [@DurationMax](#durationmaxdays-housrs-minitues-seconds-millis-nanos-inclusive)
- [@DurationMin](#durationmindays-housrs-minitues-seconds-millis-nanos-inclusive)
- [@CodePointLength](#codepointlengthmin-max-normalizationstrategy)
- [@ConstraintComposition](#constraintcompositionvalue)
- [@CreditCardNumber](#creditcardnumberignorenondigitcharacters)
- [@Currency](#currencyvalue)
- [@EAN](#eantype)
- [@ISBN](#isbntype)
- [@Length](#lengthmin-max)
- [@LuhnCheck](#luhncheckstartindex-endindex-checkdigitindex-ignorenondigitcharacters)
- [@Mod10Check](#mod10checkmultiplier-weight-startindex-endindex-checkdigitindex-ignorenondigitcharacters)
- [@Mod11Check](#mod11checkthreshold-startindex-endindex-checkdigitindex-ignorenondigitcharacters-treatcheck10as-treatcheck11as-processingdirection)
- [@ParameterScriptAssert](#parameterscriptassertlang-script)
- [@Range](#rangemin-max)
- [@ScriptAssert](#scriptassertlang-script-alias-reporton)
- [@UniqueElements](#uniqueelements)
- [@URL](#urlprotocol-host-port-regexp-flags)

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
inclusive의 default 값은 true 입니다.
```

#### @DecimalMin(value*=, inclusive=)
```
주석이 달린 요소는 value보다 크거나 같아야합니다.
지원되는 타입은 BigDecimal, BigInteger, CharSequence, 그리고 byte, short, int, long 및 각각의 래퍼입니다.
반올림 오류로 인해 double과 float는 지원되지 않습니다. (일부 제공 업체는 대략적인 지원을 제공할 수 있습니다.)
null 요소는 유효한 것으로 간주됩니다.
inclusive가 true인 경우 주석이 달린 요소는 value보다 크거나 같아야 하고, false인 경우 value보다 커야 합니다.
inclusive의 default 값은 true 입니다.
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
주석이 달린 요소의 크기는 지정된 경계를 포함한 사이에 있어야 합니다.
지원되는 타입은 CharSequence, Collection, Map, 배열입니다.
null 요소는 유효한 것으로 간주됩니다.
요소의 크기는 min보다 크거나 같아야 하고, max보다 작거나 같아야 합니다.
min의 default 값은 0, max의 default 값은 2147483647 입니다.
```

#### @CNPJ
```
CNPJ(브라질 법인 납세자 등록 번호)의 유효성을 검사합니다.
```

#### @CPF
```
CPF(브라질 개인 납세자 등록 번호)의 유효성을 검사합니다.
```

#### @TituloEleitoral
```
브라질 유권자 ID 카드 번호의 유효성을 검사합니다.
```

#### @NIP
```
CharSequence가 NIP 번호(9자리 폴란드 VAT 식별 번호)인지 확인합니다.
```

#### @PESEL
```
CharSequence가 PESEL(폴란드 국가 식별 번호)인지 확인합니다.
```

#### @REGON
```
CharSequence가 REGON 번호(9/14 자리 폴란드 납세자 식별 번호)인지 확인합니다.
```

#### @DurationMax(days=, housrs=, minitues=, seconds=, millis=, nanos=, inclusive=)
```
주석이 달린 Duration 요소는 nanos, seconds, minutes, hours, days의 합보다 작거나 같아야 합니다.
default 값은 모두 0 입니다.
inclusive가 true인 경우 주석이 달린 요소는 value보다 작거나 같아야 하고, false인 경우 value보다 작아야 합니다.
inclusive의 default 값은 true 입니다.
```

#### @DurationMin(days=, housrs=, minitues=, seconds=, millis=, nanos=, inclusive=)
```
주석이 달린 Duration 요소는 nanos, seconds, minutes, hours, days의 합보다 크거나 같아야 합니다.
default 값은 모두 0 입니다.
inclusive가 true인 경우 주석이 달린 요소는 value보다 크거나 같아야 하고, false인 경우 value보다 커야 합니다.
inclusive의 default 값은 true 입니다.
```

#### @CodePointLength(min=, max=, normalizationStrategy=)
```
CharSequence의 코드 포인트 길이가 min과 max 사이인지 확인합니다.
min의 default 값은 0, max의 default 값은 2147483647 입니다.
normalizationStrategy을 설정하여 정규화된 값을 검증할 수 있습니다.

Strategy for normalization
NONE: 정규화 없음
NFD: 표준 분해에 의한 정규화
NFC: 표준 분해에 의한 정규화, 이어서 표준 조합
NFKD: 호환성 분해에 의한 정규화
NFKC: 호환성 분해에 의한 정규화, 이어서 표준 조합
```

#### @ConstraintComposition(value=)
```
작성 제한 조건 주석의 모든 제한 조건에 적용되는 부울 연산자입니다.
구성된 제한 조건 주석을 구성하는 제한 조건의 부울 조합의 정의할 수 있습니다.
```

#### @CreditCardNumber(ignoreNonDigitCharacters=)
```
주석이 달린 요소는 유효한 신용 카드 번호를 나타내야 합니다.
이것은 신용 카드 유효성이 아닌 사용자 실수를 확인하는 것으 목표로 하는 Luhn 알고리즘 구현입니다.
ignoreNonDigitCharacters가 true인 경우 입력에서 숫자가 아니 문자를 무시하고, false인 경우 오류가 발생합니다.
ignoreNonDigitCharacters의 defulat 값은 false 입니다.
```

#### @Currency(value=)

#### @EAN(type=)
```
주석이 달린 CharSequence가 유효한 EAN 13 번호인지 확인합니다.
숫자의 길이와 숫자가 확인됩니다.
null은 유효한 것으로 간주됩니다.
```

#### @ISBN(type=)
```
주석이 달린 CharSequence가 유효한 ISBN인지 확인합니다.
숫자의 길이와 숫자가 모두 확인됩니다.
null은 유효한 것으로 간주됩니다.
유효성 검사 중에 ISBN 문자가 아닌 것들은 무시됩니다.
모든 숫자와 X가 유효한 ISBN 문자로 간주됩니다.
이는 숫자를 구분하는 대시가 있는 ISBN을 확인할 때 유용합니다. (ex. 978-161-729-045-9)
type은 ISBN의 길이를 정의합니다.
유효한 길이는 10과 13으로 각각 ISBN_10과 ISBN_13으로 표시됩니다.
type의 default 값은 ISBN_13 입니다.
```

#### @Length(min=, max=)
```
문자열의 길이가 min과 max 사이인지 확인합니다.
min의 default 값은 0, max의 default 값은 2147483647 입니다.
```

#### @LuhnCheck(startIndex=, endIndex=, checkDigitIndex=, ignoreNonDigitCharacters=)
```
startIndex의 default 값은 0, endIndex의 default 값은 2147483647, 
checkDigitIndex의 default 값은 -1, ignoreNonDigitCharacters의 default 값은 true 입니다.
```

#### @Mod10Check(multiplier=, weight=, startIndex=, endIndex=, checkDigitIndex=, ignoreNonDigitCharacters=)
```
multiplier의 default 값은 3, weight의 default 값은 1,
startIndex의 default 값은 0, endIndex의 default 값은 2147483647, 
checkDigitIndex의 default 값은 -1, ignoreNonDigitCharacters의 default 값은 true 입니다.
```

#### @Mod11Check(threshold=, startIndex=, endIndex=, checkDigitIndex=, ignoreNonDigitCharacters=, treatCheck10As, treatCheck11As=, processingDirection=)
```
threshold의 default 값은 2147483647, startIndex의 default 값은 0, endIndex의 default 값은 2147483647, 
checkDigitIndex의 default 값은 -1, checkDigitIndex의 default 값은 -1, ignoreNonDigitCharacters의 default 값은 true,
treatCheck10As의 default 값은 'X', treatCheck11As의 default 값은 '0', processingDirectiondml default 값은 RIGHT_TO_LEFT 입니다.
```

#### @ParameterScriptAssert(lang*=, script*=)

#### @Range(min=, max=)
```
주석이 달린 요소는 적절한 범위 내에 있어야 합니다.
숫자 값 또는 숫자 값의 문자열 표현에 적용할 수 있습니다.
min의 default 값은 0L, max의 default 값은 9223372036854775807L 입니다.
```

#### @ScriptAssert(lang*=, script*=, alias=, reportOn=)
```
alias의 default 값은 "_this" 입니다.
```

#### @UniqueElements
```
주석이 달린 Collection의 모든 객체가 고유한지 확인합니다.
즉, 동일한 요소르 찾을 수 없습니다.
예를 들어, JAX-RS에서 유용합니다.
JAX-RS는 항상 컬렉션을 list로 비직렬화합니다.
그러므로 set으로 변환할때 중복이 내재적으로 제거됩니다.
이 제약 조건을 사용하면 list에서 중복을 확인하고 대시 오류를 발생시킬 수 있습니다.
```

#### @URL(protocol=, host=, port=, regexp=, flags=)
```
주석이 달린 문자열이 URL인지 확인합니다.
매개변수 protocol, host, port는 URL의 해당 부분과 매칭됩니다.
추가 정규식은 regexp와 flags를 사용하여 지정할 수 있습니다.
기본적으로 이 제약 조건에 대한 유효성 검증은 java.net.URL 생성자를 사용하여 문자열의 유효성을 검증합니다.
이는 일치하는 프로토콜 처리기를 사용할 수 있어야 함을 의미합니다.
다음 프로토콜에 대한 처리자는 기본 JVM 내에 존재하는 http, https, ftp, ftp, file 및 jar를 보장합니다.
```

**사용 예시**

```java
@Getter
public class RequestDto {

    @URL(message = "유효한 URL 값이 아닙니다.")
    private String url;

    @URL(message = "깃허브 주소가 아닙니다.", protocol = "https", host = "github.com")
    private String githubUrl;
}

```

```java
@RestController
public class Controller {

    @PostMapping
    public ResponseEntity<Void> test(@Valid @RequestBody RequestDto requestDto) {
        return ResponseEntity.status(HttpStatus.OK).build();
    }
}
```

**테스트 코드**

```java
@RunWith(SpringRunner.class)
@WebMvcTest(Controller.class)
public class ControllerTest {

    @Autowired
    private MockMvc mockMvc;

    @Test
    public void validURL() throws Exception {
        mockMvc.perform(post("")
                .contentType(MediaType.APPLICATION_JSON)
                .content("{\"url\":\"http://www.naver.com\"}"))
                .andExpect(status().isOk());
    }


    @Test
    public void invalidURL() throws Exception {
        mockMvc.perform(post("")
                .contentType(MediaType.APPLICATION_JSON)
                .content("{\"url\":\"naver\"}"))
                .andExpect(status().isBadRequest());
    }

    @Test
    public void validGithubURL() throws Exception {
        mockMvc.perform(post("")
                .contentType(MediaType.APPLICATION_JSON)
                .content("{\"githubUrl\":\"https://github.com/HyeranShin\"}"))
                .andExpect(status().isOk());
    }

    @Test
    public void invalidGithubURL() throws Exception {
        mockMvc.perform(post("")
                .contentType(MediaType.APPLICATION_JSON)
                .content("{\"githubUrl\":\"http://www.naver.com\"}"))
                .andExpect(status().isBadRequest());
    }
}
```
